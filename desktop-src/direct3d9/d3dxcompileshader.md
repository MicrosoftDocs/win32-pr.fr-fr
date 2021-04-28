---
description: D3DXCompileShader fonction-compile un fichier de nuanceur.
ms.assetid: 9b19ab67-d5d5-482d-b3fe-ce20b64d7ad8
title: D3DXCompileShader, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b1f5e5f0f30714ed001438235e124341b8ce4d35
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115857"
---
# <a name="d3dxcompileshader-function"></a><span data-ttu-id="1def0-103">D3DXCompileShader fonction)</span><span class="sxs-lookup"><span data-stu-id="1def0-103">D3DXCompileShader function</span></span>

<span data-ttu-id="1def0-104">Compilez un fichier de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="1def0-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="1def0-105">Au lieu d’utiliser cette fonction héritée, nous vous recommandons de compiler hors connexion à l’aide du compilateur de ligne de commande Fxc.exe ou d’utiliser l’API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="1def0-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1def0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1def0-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShader(
  _In_        LPCSTR              pSrcData,
  _In_        UINT                srcDataLen,
  _In_  const D3DXMACRO           *pDefines,
  _In_        LPD3DXINCLUDE       pInclude,
  _In_        LPCSTR              pFunctionName,
  _In_        LPCSTR              pProfile,
  _In_        DWORD               Flags,
  _Out_       LPD3DXBUFFER        *ppShader,
  _Out_       LPD3DXBUFFER        *ppErrorMsgs,
  _Out_       LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="1def0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1def0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1def0-108">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1def0-108">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1def0-109">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1def0-109">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1def0-110">Pointeur vers une chaîne qui contient le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="1def0-110">Pointer to a string that contains the shader.</span></span>

</dd> <dt>

<span data-ttu-id="1def0-111">*srcDataLen* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1def0-111">*srcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1def0-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1def0-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1def0-113">Longueur des données en octets.</span><span class="sxs-lookup"><span data-stu-id="1def0-113">Length of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1def0-114">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1def0-114">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1def0-115">Type : **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="1def0-115">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="1def0-116">Tableau de structures [**D3DXMACRO**](d3dxmacro.md) terminé par un caractère **null** facultatif.</span><span class="sxs-lookup"><span data-stu-id="1def0-116">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="1def0-117">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="1def0-117">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1def0-118">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1def0-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1def0-119">Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="1def0-119">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="1def0-120">Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include.</span><span class="sxs-lookup"><span data-stu-id="1def0-120">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="1def0-121">Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.</span><span class="sxs-lookup"><span data-stu-id="1def0-121">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="1def0-122">*pFunctionName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1def0-122">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1def0-123">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1def0-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1def0-124">Pointeur vers une chaîne qui contient le nom de la fonction de point d’entrée du nuanceur au début de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="1def0-124">Pointer to a string that contains the name of the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="1def0-125">*pProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1def0-125">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1def0-126">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1def0-126">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1def0-127">Pointeur vers un profil de nuanceur qui détermine le jeu d’instructions du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="1def0-127">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="1def0-128">Pour obtenir la liste des profils disponibles, consultez [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) ou [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="1def0-128">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="1def0-129">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="1def0-129">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1def0-130">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1def0-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1def0-131">Options de compilation identifiées par différents indicateurs.</span><span class="sxs-lookup"><span data-stu-id="1def0-131">Compile options identified by various flags.</span></span> <span data-ttu-id="1def0-132">Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="1def0-132">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="1def0-133">Pour plus d’informations, consultez [indicateurs D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="1def0-133">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="1def0-134">*ppShader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1def0-134">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1def0-135">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1def0-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1def0-136">Retourne une mémoire tampon contenant le nuanceur créé.</span><span class="sxs-lookup"><span data-stu-id="1def0-136">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="1def0-137">Cette mémoire tampon contient le code de nuanceur compilé, ainsi que toutes les informations de débogage et de table de symboles incorporées.</span><span class="sxs-lookup"><span data-stu-id="1def0-137">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="1def0-138">*ppErrorMsgs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1def0-138">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1def0-139">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1def0-139">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1def0-140">Retourne une mémoire tampon qui contient une liste d’erreurs et d’avertissements qui ont été rencontrés pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="1def0-140">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="1def0-141">Ce sont les mêmes messages que le débogueur affiche lorsqu’il s’exécute en mode débogage.</span><span class="sxs-lookup"><span data-stu-id="1def0-141">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="1def0-142">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="1def0-142">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1def0-143">*ppConstantTable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1def0-143">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1def0-144">Type : **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="1def0-144">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="1def0-145">Retourne une interface [**ID3DXConstantTable**](id3dxconstanttable.md) , qui peut être utilisée pour accéder aux constantes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="1def0-145">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="1def0-146">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="1def0-146">This value can be **NULL**.</span></span> <span data-ttu-id="1def0-147">Si vous compilez votre application en prenant en charge les adresses de grande taille (autrement dit, si vous utilisez l’option de l’éditeur de liens/LARGEADDRESSAWARE pour gérer les adresses supérieures à 2 Go), vous ne pouvez pas utiliser ce paramètre et devez lui affecter la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1def0-147">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="1def0-148">Au lieu de cela, vous devez utiliser la fonction [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) pour récupérer la table de nuanceur-constante incorporée dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="1def0-148">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="1def0-149">Dans cet appel **D3DXGetShaderConstantTableEx** , vous devez passer l' **indicateur \_ LARGEADDRESSAWARE D3DXCONSTTABLE** au paramètre *Flags* pour spécifier l’accès à un espace d’adressage virtuel pouvant atteindre 4 Go.</span><span class="sxs-lookup"><span data-stu-id="1def0-149">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1def0-150">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1def0-150">Return value</span></span>

<span data-ttu-id="1def0-151">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1def0-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1def0-152">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1def0-152">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1def0-153">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1def0-153">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1def0-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1def0-154">Requirements</span></span>



| <span data-ttu-id="1def0-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1def0-155">Requirement</span></span> | <span data-ttu-id="1def0-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="1def0-156">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1def0-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="1def0-157">Header</span></span><br/>  | <dl> <span data-ttu-id="1def0-158"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1def0-158"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1def0-159">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1def0-159">Library</span></span><br/> | <dl> <span data-ttu-id="1def0-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1def0-160"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1def0-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1def0-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1def0-162">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="1def0-162">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="1def0-163">**D3DXCompileShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="1def0-163">**D3DXCompileShaderFromFile**</span></span>](d3dxcompileshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="1def0-164">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="1def0-164">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
