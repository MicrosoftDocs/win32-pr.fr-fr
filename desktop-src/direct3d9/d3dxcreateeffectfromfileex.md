---
description: Créer un effet à partir d’une description d’effet ASCII ou binaire. Cette fonction est une version étendue de D3DXCreateEffectFromFile qui permet à une application de contrôler les paramètres qui sont ignorés par le système d’effets.
ms.assetid: 963caa1e-bc1a-4d4b-bdb1-50b17d8b4132
title: D3DXCreateEffectFromFileEx, fonction (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFileEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b3d97c5aa23dd0711cfb00585e5b8ba7d410fc02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539909"
---
# <a name="d3dxcreateeffectfromfileex-function"></a><span data-ttu-id="c9c0b-104">D3DXCreateEffectFromFileEx fonction)</span><span class="sxs-lookup"><span data-stu-id="c9c0b-104">D3DXCreateEffectFromFileEx function</span></span>

<span data-ttu-id="c9c0b-105">Créer un effet à partir d’une description d’effet ASCII ou binaire.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-105">Create an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="c9c0b-106">Cette fonction est une version étendue de [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) qui permet à une application de contrôler les paramètres qui sont ignorés par le système d’effets.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-106">This function is an extended version of [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9c0b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9c0b-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromFileEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="c9c0b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9c0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9c0b-109">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9c0b-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9c0b-110">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c9c0b-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c9c0b-111">Pointeur vers l’appareil qui va créer l’effet.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-111">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="c9c0b-112">Consultez [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="c9c0b-112">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="c9c0b-113">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9c0b-113">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9c0b-114">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9c0b-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9c0b-115">Pointeur vers le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-115">Pointer to the filename.</span></span> <span data-ttu-id="c9c0b-116">Ce paramètre prend en charge les chaînes Unicode et ANSI.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-116">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="c9c0b-117">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c9c0b-118">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9c0b-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9c0b-119">Type : **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="c9c0b-119">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="c9c0b-120">Tableau de définitions de macros de préprocesseur se terminant par un caractère NULL facultatif.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-120">Optional NULL-terminated array of preprocessor macro definitions.</span></span> <span data-ttu-id="c9c0b-121">Consultez [**D3DXMACRO**](d3dxmacro.md).</span><span class="sxs-lookup"><span data-stu-id="c9c0b-121">See [**D3DXMACRO**](d3dxmacro.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9c0b-122">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9c0b-122">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9c0b-123">Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="c9c0b-123">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="c9c0b-124">Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-124">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="c9c0b-125">Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-125">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="c9c0b-126">*pSkipConstants* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9c0b-126">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9c0b-127">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9c0b-127">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9c0b-128">Chaîne de paramètres d’effet qui sera ignorée par le système d’effet.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-128">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="c9c0b-129">La chaîne doit se terminer par une **valeur null** et doit contenir le nom de chaque constante gérée par l’application, séparées par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-129">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="c9c0b-130">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="c9c0b-130">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9c0b-131">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9c0b-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9c0b-132">Si *pSrcFile* contient un effet de texte, Flags peut être une combinaison d' [indicateurs D3DXSHADER](d3dxshader-flags.md) et d’indicateurs [D3DXFX](d3dxfx.md) ; Sinon, *pSrcFile* contient un effet binaire et les seuls indicateurs honorés sont des indicateurs D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-132">If *pSrcFile* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcFile* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="c9c0b-133">Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-133">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="c9c0b-134">Pour plus d’informations [, consultez outil de compilateur Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="c9c0b-134">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="c9c0b-135">*pPool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9c0b-135">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9c0b-136">Type : **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="c9c0b-136">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="c9c0b-137">Pointeur vers un objet [**ID3DXEffectPool**](id3dxeffectpool.md) à utiliser pour les paramètres partagés.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-137">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="c9c0b-138">Si cette valeur est **null**, aucun paramètre n’est partagé.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-138">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="c9c0b-139">*ppEffect* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c9c0b-139">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9c0b-140">Type : **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9c0b-140">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="c9c0b-141">Retourne un pointeur vers une mémoire tampon contenant l’effet compilé.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-141">Returns a pointer to a buffer containing the compiled effect.</span></span> <span data-ttu-id="c9c0b-142">Consultez [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="c9c0b-142">See [**ID3DXEffect**](id3dxeffect.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9c0b-143">*ppCompilationErrors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c9c0b-143">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9c0b-144">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9c0b-144">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c9c0b-145">Retourne un pointeur vers une mémoire tampon contenant une liste d’erreurs de compilation.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-145">Returns a pointer to a buffer containing a listing of compile errors.</span></span> <span data-ttu-id="c9c0b-146">Consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="c9c0b-146">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9c0b-147">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9c0b-147">Return value</span></span>

<span data-ttu-id="c9c0b-148">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c9c0b-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c9c0b-149">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c9c0b-150">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-150">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9c0b-151">Notes</span><span class="sxs-lookup"><span data-stu-id="c9c0b-151">Remarks</span></span>

<span data-ttu-id="c9c0b-152">Cette fonction est une version étendue de [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) qui permet à une application de spécifier les constantes d’effet qui seront gérées par l’application.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-152">This function is an extended version of [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="c9c0b-153">Une constante gérée par l’application est ignorée par le système d’effets.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-153">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="c9c0b-154">Autrement dit, l’application est responsable de l’initialisation de la constante, ainsi que de l’enregistrement et de la restauration de son état chaque fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-154">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="c9c0b-155">Cette fonction vérifie chaque constante dans pSkipConstants pour voir ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="c9c0b-155">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="c9c0b-156">Elle est liée à un registre de constantes.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-156">It is bound to a constant register.</span></span>
-   <span data-ttu-id="c9c0b-157">Il est utilisé uniquement dans le code de nuanceur HLSL.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-157">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="c9c0b-158">Si une constante est nommée dans la chaîne qui n’est pas présente dans l’effet, elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-158">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

<span data-ttu-id="c9c0b-159">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-159">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="c9c0b-160">Dans le cas contraire, le type de données LPCTSTR est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-160">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="c9c0b-161">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-161">The compiler setting also determines the function version.</span></span> <span data-ttu-id="c9c0b-162">Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateEffectFromFileW.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-162">If Unicode is defined, the function call resolves to D3DXCreateEffectFromFileW.</span></span> <span data-ttu-id="c9c0b-163">Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateEffectFromFileA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="c9c0b-163">Otherwise, the function call resolves to D3DXCreateEffectFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9c0b-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9c0b-164">Requirements</span></span>



| <span data-ttu-id="c9c0b-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9c0b-165">Requirement</span></span> | <span data-ttu-id="c9c0b-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9c0b-166">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9c0b-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9c0b-167">Header</span></span><br/>  | <dl> <span data-ttu-id="c9c0b-168"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9c0b-168"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c9c0b-169">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c9c0b-169">Library</span></span><br/> | <dl> <span data-ttu-id="c9c0b-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9c0b-170"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c9c0b-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9c0b-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9c0b-172">Fonctions Effect</span><span class="sxs-lookup"><span data-stu-id="c9c0b-172">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="c9c0b-173">**D3DXCreateEffectEx**</span><span class="sxs-lookup"><span data-stu-id="c9c0b-173">**D3DXCreateEffectEx**</span></span>](d3dxcreateeffectex.md)
</dt> <dt>

[<span data-ttu-id="c9c0b-174">**D3DXCreateEffectFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="c9c0b-174">**D3DXCreateEffectFromResourceEx**</span></span>](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
