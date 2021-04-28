---
description: 'Fonction D3DXCreateEffectFromFile : créez un effet à partir d’une description d’effet ASCII ou binaire.'
ms.assetid: b5868ba3-0869-46f7-804f-3103358a3ef5
title: D3DXCreateEffectFromFile, fonction (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d8b2afdd1e8008bc8e03efa670e5a4b37b6dc9f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094317"
---
# <a name="d3dxcreateeffectfromfile-function"></a><span data-ttu-id="7ec90-103">D3DXCreateEffectFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="7ec90-103">D3DXCreateEffectFromFile function</span></span>

<span data-ttu-id="7ec90-104">Créer un effet à partir d’une description d’effet ASCII ou binaire.</span><span class="sxs-lookup"><span data-stu-id="7ec90-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec90-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ec90-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromFile(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="7ec90-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ec90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ec90-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ec90-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec90-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7ec90-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7ec90-109">Pointeur vers l’appareil qui va créer l’effet.</span><span class="sxs-lookup"><span data-stu-id="7ec90-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="7ec90-110">Consultez [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="7ec90-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="7ec90-111">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ec90-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec90-112">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ec90-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ec90-113">Pointeur vers le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="7ec90-113">Pointer to the filename.</span></span> <span data-ttu-id="7ec90-114">Ce paramètre prend en charge les chaînes Unicode et ANSI.</span><span class="sxs-lookup"><span data-stu-id="7ec90-114">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="7ec90-115">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="7ec90-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7ec90-116">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ec90-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec90-117">Type : **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="7ec90-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="7ec90-118">Tableau de définitions de macros de préprocesseur se terminant par un caractère NULL facultatif.</span><span class="sxs-lookup"><span data-stu-id="7ec90-118">Optional NULL-terminated array of preprocessor macro definitions.</span></span> <span data-ttu-id="7ec90-119">Consultez [**D3DXMACRO**](d3dxmacro.md).</span><span class="sxs-lookup"><span data-stu-id="7ec90-119">See [**D3DXMACRO**](d3dxmacro.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ec90-120">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ec90-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec90-121">Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="7ec90-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="7ec90-122">Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include.</span><span class="sxs-lookup"><span data-stu-id="7ec90-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="7ec90-123">Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.</span><span class="sxs-lookup"><span data-stu-id="7ec90-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="7ec90-124">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="7ec90-124">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec90-125">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ec90-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ec90-126">Si *pSrcFile* contient un effet de texte, Flags peut être une combinaison d' [indicateurs D3DXSHADER](d3dxshader-flags.md) et d’indicateurs [D3DXFX](d3dxfx.md) ; Sinon, *pSrcFile* contient un effet binaire et les seuls indicateurs honorés sont des indicateurs D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="7ec90-126">If *pSrcFile* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcFile* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="7ec90-127">Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ec90-127">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="7ec90-128">Pour plus d’informations [, consultez outil de compilateur Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="7ec90-128">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="7ec90-129">*pPool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ec90-129">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec90-130">Type : **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="7ec90-130">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="7ec90-131">Pointeur vers un objet [**ID3DXEffectPool**](id3dxeffectpool.md) à utiliser pour les paramètres partagés.</span><span class="sxs-lookup"><span data-stu-id="7ec90-131">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="7ec90-132">Si cette valeur est **null**, aucun paramètre n’est partagé.</span><span class="sxs-lookup"><span data-stu-id="7ec90-132">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="7ec90-133">*ppEffect* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7ec90-133">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec90-134">Type : **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ec90-134">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="7ec90-135">Retourne un pointeur vers une mémoire tampon contenant l’effet compilé.</span><span class="sxs-lookup"><span data-stu-id="7ec90-135">Returns a pointer to a buffer containing the compiled effect.</span></span> <span data-ttu-id="7ec90-136">Consultez [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="7ec90-136">See [**ID3DXEffect**](id3dxeffect.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ec90-137">*ppCompilationErrors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7ec90-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec90-138">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ec90-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7ec90-139">Retourne un pointeur vers une mémoire tampon contenant une liste d’erreurs de compilation.</span><span class="sxs-lookup"><span data-stu-id="7ec90-139">Returns a pointer to a buffer containing a listing of compile errors.</span></span> <span data-ttu-id="7ec90-140">Consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="7ec90-140">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ec90-141">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7ec90-141">Return value</span></span>

<span data-ttu-id="7ec90-142">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ec90-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ec90-143">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7ec90-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7ec90-144">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7ec90-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ec90-145">Notes </span><span class="sxs-lookup"><span data-stu-id="7ec90-145">Remarks</span></span>

<span data-ttu-id="7ec90-146">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="7ec90-146">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="7ec90-147">Dans le cas contraire, le type de données LPCTSTR est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="7ec90-147">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="7ec90-148">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="7ec90-148">The compiler setting also determines the function version.</span></span> <span data-ttu-id="7ec90-149">Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateEffectFromFileW.</span><span class="sxs-lookup"><span data-stu-id="7ec90-149">If Unicode is defined, the function call resolves to D3DXCreateEffectFromFileW.</span></span> <span data-ttu-id="7ec90-150">Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateEffectFromFileA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="7ec90-150">Otherwise, the function call resolves to D3DXCreateEffectFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ec90-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ec90-151">Requirements</span></span>



| <span data-ttu-id="7ec90-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ec90-152">Requirement</span></span> | <span data-ttu-id="7ec90-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ec90-153">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec90-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ec90-154">Header</span></span><br/>  | <dl> <span data-ttu-id="7ec90-155"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ec90-155"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7ec90-156">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7ec90-156">Library</span></span><br/> | <dl> <span data-ttu-id="7ec90-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ec90-157"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7ec90-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ec90-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ec90-159">Fonctions Effect</span><span class="sxs-lookup"><span data-stu-id="7ec90-159">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="7ec90-160">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="7ec90-160">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="7ec90-161">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="7ec90-161">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
