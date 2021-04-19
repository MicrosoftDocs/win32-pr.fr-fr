---
description: Créer un effet à partir d’une description d’effet ASCII ou binaire.
ms.assetid: 8385512c-e93d-4c07-b353-87717eb58bcd
title: D3DXCreateEffectFromResource, fonction (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 36db2c82debc542301ba44d4baa74ecaaf01245e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535831"
---
# <a name="d3dxcreateeffectfromresource-function"></a><span data-ttu-id="521e0-103">D3DXCreateEffectFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="521e0-103">D3DXCreateEffectFromResource function</span></span>

<span data-ttu-id="521e0-104">Créer un effet à partir d’une description d’effet ASCII ou binaire.</span><span class="sxs-lookup"><span data-stu-id="521e0-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="521e0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="521e0-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromResource(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="521e0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="521e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="521e0-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="521e0-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="521e0-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="521e0-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="521e0-109">Pointeur vers l’appareil.</span><span class="sxs-lookup"><span data-stu-id="521e0-109">Pointer to the device.</span></span>

</dd> <dt>

<span data-ttu-id="521e0-110">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="521e0-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="521e0-111">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="521e0-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="521e0-112">Handle d’un module contenant la description de l’effet.</span><span class="sxs-lookup"><span data-stu-id="521e0-112">Handle to a module containing the effect description.</span></span> <span data-ttu-id="521e0-113">Si ce paramètre a la **valeur null**, le module actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="521e0-113">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="521e0-114">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="521e0-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="521e0-115">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="521e0-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="521e0-116">Pointeur vers la ressource.</span><span class="sxs-lookup"><span data-stu-id="521e0-116">Pointer to the resource.</span></span> <span data-ttu-id="521e0-117">Ce paramètre prend en charge les chaînes Unicode et ANSI.</span><span class="sxs-lookup"><span data-stu-id="521e0-117">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="521e0-118">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="521e0-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="521e0-119">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="521e0-119">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="521e0-120">Type : **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="521e0-120">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="521e0-121">Tableau de structures [**D3DXMACRO**](d3dxmacro.md) se terminant par un caractère **null** facultatif qui décrivent les définitions de préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="521e0-121">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="521e0-122">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="521e0-122">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="521e0-123">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="521e0-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="521e0-124">Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="521e0-124">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="521e0-125">Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include.</span><span class="sxs-lookup"><span data-stu-id="521e0-125">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="521e0-126">Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.</span><span class="sxs-lookup"><span data-stu-id="521e0-126">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="521e0-127">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="521e0-127">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="521e0-128">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="521e0-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="521e0-129">Si *hSrcModule* contient un effet de texte, Flags peut être une combinaison d' [indicateurs D3DXSHADER](d3dxshader-flags.md) et d’indicateurs [D3DXFX](d3dxfx.md) ; Sinon, *hSrcModule* contient un effet binaire et les seuls indicateurs honorés sont des indicateurs D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="521e0-129">If *hSrcModule* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *hSrcModule* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="521e0-130">Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="521e0-130">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="521e0-131">Pour plus d’informations [, consultez outil de compilateur Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="521e0-131">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="521e0-132">*pPool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="521e0-132">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="521e0-133">Type : **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="521e0-133">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="521e0-134">Pointeur vers un objet [**ID3DXEffectPool**](id3dxeffectpool.md) à utiliser pour les paramètres partagés.</span><span class="sxs-lookup"><span data-stu-id="521e0-134">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="521e0-135">Si cette valeur est **null**, aucun paramètre n’est partagé.</span><span class="sxs-lookup"><span data-stu-id="521e0-135">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="521e0-136">*ppEffect* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="521e0-136">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="521e0-137">Type : **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="521e0-137">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="521e0-138">Retourne une mémoire tampon contenant l’effet compilé.</span><span class="sxs-lookup"><span data-stu-id="521e0-138">Returns a buffer containing the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="521e0-139">*ppCompilationErrors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="521e0-139">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="521e0-140">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="521e0-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="521e0-141">Retourne une mémoire tampon qui contient une liste d’erreurs de compilation.</span><span class="sxs-lookup"><span data-stu-id="521e0-141">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="521e0-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="521e0-142">Return value</span></span>

<span data-ttu-id="521e0-143">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="521e0-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="521e0-144">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="521e0-144">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="521e0-145">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="521e0-145">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="521e0-146">Notes</span><span class="sxs-lookup"><span data-stu-id="521e0-146">Remarks</span></span>

<span data-ttu-id="521e0-147">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="521e0-147">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="521e0-148">Dans le cas contraire, le type de données LPCTSTR est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="521e0-148">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="521e0-149">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="521e0-149">The compiler setting also determines the function version.</span></span> <span data-ttu-id="521e0-150">Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateEffectFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="521e0-150">If Unicode is defined, the function call resolves to D3DXCreateEffectFromResourceW.</span></span> <span data-ttu-id="521e0-151">Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateEffectFromResourceA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="521e0-151">Otherwise, the function call resolves to D3DXCreateEffectFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="521e0-152">D3DXCreateEffectFromResource charge des données à partir d’une ressource de type RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="521e0-152">D3DXCreateEffectFromResource loads data from a resource of type RT\_RCDATA.</span></span> <span data-ttu-id="521e0-153">Pour plus d’informations sur les ressources Windows, consultez MSDN.</span><span class="sxs-lookup"><span data-stu-id="521e0-153">See MSDN for more information about Windows resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="521e0-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="521e0-154">Requirements</span></span>



| <span data-ttu-id="521e0-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="521e0-155">Requirement</span></span> | <span data-ttu-id="521e0-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="521e0-156">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="521e0-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="521e0-157">Header</span></span><br/>  | <dl> <span data-ttu-id="521e0-158"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="521e0-158"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="521e0-159">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="521e0-159">Library</span></span><br/> | <dl> <span data-ttu-id="521e0-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="521e0-160"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="521e0-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="521e0-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="521e0-162">Fonctions Effect</span><span class="sxs-lookup"><span data-stu-id="521e0-162">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="521e0-163">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="521e0-163">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="521e0-164">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="521e0-164">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
