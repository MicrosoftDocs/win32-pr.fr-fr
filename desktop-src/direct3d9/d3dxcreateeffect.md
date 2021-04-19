---
description: Créer un effet à partir d’une description d’effet ASCII ou binaire.
ms.assetid: 1cbd91f2-3cda-4770-a3c5-b1e6702628d1
title: D3DXCreateEffect, fonction (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3d5ac013617368ba4d702815d79aa411ea2988b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522359"
---
# <a name="d3dxcreateeffect-function"></a><span data-ttu-id="8a796-103">D3DXCreateEffect fonction)</span><span class="sxs-lookup"><span data-stu-id="8a796-103">D3DXCreateEffect function</span></span>

<span data-ttu-id="8a796-104">Créer un effet à partir d’une description d’effet ASCII ou binaire.</span><span class="sxs-lookup"><span data-stu-id="8a796-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a796-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a796-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="8a796-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a796-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a796-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a796-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a796-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="8a796-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="8a796-109">Pointeur vers l’appareil qui va créer l’effet.</span><span class="sxs-lookup"><span data-stu-id="8a796-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="8a796-110">Consultez [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="8a796-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="8a796-111">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a796-111">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a796-112">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a796-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a796-113">Pointeur vers une mémoire tampon qui contient une description d’effet.</span><span class="sxs-lookup"><span data-stu-id="8a796-113">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="8a796-114">*SrcDataLen* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a796-114">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a796-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a796-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a796-116">Longueur des données d’effet, en octets.</span><span class="sxs-lookup"><span data-stu-id="8a796-116">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8a796-117">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a796-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a796-118">Type : **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="8a796-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="8a796-119">Tableau de structures [**D3DXMACRO**](d3dxmacro.md) se terminant par un caractère **null** facultatif qui décrivent les définitions de préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="8a796-119">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="8a796-120">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="8a796-120">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8a796-121">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a796-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a796-122">Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="8a796-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="8a796-123">Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include.</span><span class="sxs-lookup"><span data-stu-id="8a796-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="8a796-124">Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.</span><span class="sxs-lookup"><span data-stu-id="8a796-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="8a796-125">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="8a796-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a796-126">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a796-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a796-127">Si *pSrcData* contient un effet de texte, Flags peut être une combinaison d' [indicateurs D3DXSHADER](d3dxshader-flags.md) et d’indicateurs [D3DXFX](d3dxfx.md) ; Sinon, *pSrcData* contient un effet binaire et les seuls indicateurs honorés sont des indicateurs D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="8a796-127">If *pSrcData* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcData* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="8a796-128">Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="8a796-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="8a796-129">Pour plus d’informations [, consultez outil de compilateur Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="8a796-129">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="8a796-130">*pPool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a796-130">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a796-131">Type : **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="8a796-131">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="8a796-132">Pointeur vers un objet [**ID3DXEffectPool**](id3dxeffectpool.md) à utiliser pour les paramètres partagés.</span><span class="sxs-lookup"><span data-stu-id="8a796-132">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="8a796-133">Si cette valeur est **null**, aucun paramètre n’est partagé.</span><span class="sxs-lookup"><span data-stu-id="8a796-133">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="8a796-134">*ppEffect* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8a796-134">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a796-135">Type : **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a796-135">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="8a796-136">Retourne un pointeur vers une interface [**ID3DXEffect**](id3dxeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="8a796-136">Returns a pointer to an [**ID3DXEffect**](id3dxeffect.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="8a796-137">*ppCompilationErrors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8a796-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a796-138">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a796-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8a796-139">Retourne une mémoire tampon qui contient une liste d’erreurs de compilation.</span><span class="sxs-lookup"><span data-stu-id="8a796-139">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a796-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a796-140">Return value</span></span>

<span data-ttu-id="8a796-141">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8a796-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8a796-142">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8a796-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8a796-143">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8a796-143">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a796-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a796-144">Requirements</span></span>



| <span data-ttu-id="8a796-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a796-145">Requirement</span></span> | <span data-ttu-id="8a796-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a796-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a796-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a796-147">Header</span></span><br/>  | <dl> <span data-ttu-id="8a796-148"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a796-148"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="8a796-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8a796-149">Library</span></span><br/> | <dl> <span data-ttu-id="8a796-150"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a796-150"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8a796-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a796-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a796-152">Fonctions Effect</span><span class="sxs-lookup"><span data-stu-id="8a796-152">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="8a796-153">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="8a796-153">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="8a796-154">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="8a796-154">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
