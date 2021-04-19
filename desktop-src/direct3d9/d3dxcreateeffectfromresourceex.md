---
description: Créer un effet à partir d’une description d’effet ASCII ou binaire. Il s’agit d’une version étendue de D3DXCreateEffectFromResource qui permet à une application de contrôler les paramètres qui sont ignorés par le système d’effets.
ms.assetid: 5937bdb1-750a-41f8-a49d-3643427f3e3c
title: D3DXCreateEffectFromResourceEx, fonction (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResourceEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d0ae7a0ee43f93019f3c4c1f6145b3d8aa0e4367
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523846"
---
# <a name="d3dxcreateeffectfromresourceex-function"></a><span data-ttu-id="01fcb-104">D3DXCreateEffectFromResourceEx fonction)</span><span class="sxs-lookup"><span data-stu-id="01fcb-104">D3DXCreateEffectFromResourceEx function</span></span>

<span data-ttu-id="01fcb-105">Créer un effet à partir d’une description d’effet ASCII ou binaire.</span><span class="sxs-lookup"><span data-stu-id="01fcb-105">Create an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="01fcb-106">Il s’agit d’une version étendue de [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) qui permet à une application de contrôler les paramètres qui sont ignorés par le système d’effets.</span><span class="sxs-lookup"><span data-stu-id="01fcb-106">This is an extended version of [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="01fcb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01fcb-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromResourceEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="01fcb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01fcb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01fcb-109">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01fcb-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01fcb-110">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="01fcb-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="01fcb-111">Pointeur vers l’appareil.</span><span class="sxs-lookup"><span data-stu-id="01fcb-111">Pointer to the device.</span></span>

</dd> <dt>

<span data-ttu-id="01fcb-112">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01fcb-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01fcb-113">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="01fcb-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="01fcb-114">Handle d’un module contenant la description de l’effet.</span><span class="sxs-lookup"><span data-stu-id="01fcb-114">Handle to a module containing the effect description.</span></span> <span data-ttu-id="01fcb-115">Si ce paramètre a la **valeur null**, le module actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="01fcb-115">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="01fcb-116">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01fcb-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01fcb-117">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="01fcb-117">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="01fcb-118">Pointeur vers la ressource.</span><span class="sxs-lookup"><span data-stu-id="01fcb-118">Pointer to the resource.</span></span> <span data-ttu-id="01fcb-119">Ce paramètre prend en charge les chaînes Unicode et ANSI.</span><span class="sxs-lookup"><span data-stu-id="01fcb-119">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="01fcb-120">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="01fcb-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="01fcb-121">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01fcb-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01fcb-122">Type : **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="01fcb-122">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="01fcb-123">Tableau de structures [**D3DXMACRO**](d3dxmacro.md) se terminant par un caractère **null** facultatif qui décrivent les définitions de préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="01fcb-123">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="01fcb-124">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="01fcb-124">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="01fcb-125">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01fcb-125">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01fcb-126">Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="01fcb-126">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="01fcb-127">Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include.</span><span class="sxs-lookup"><span data-stu-id="01fcb-127">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="01fcb-128">Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.</span><span class="sxs-lookup"><span data-stu-id="01fcb-128">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="01fcb-129">*pSkipConstants* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01fcb-129">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01fcb-130">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="01fcb-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="01fcb-131">Chaîne de paramètres d’effet qui sera ignorée par le système d’effet.</span><span class="sxs-lookup"><span data-stu-id="01fcb-131">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="01fcb-132">La chaîne doit se terminer par une **valeur null** et doit contenir le nom de chaque constante gérée par l’application, séparées par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="01fcb-132">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="01fcb-133">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="01fcb-133">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01fcb-134">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="01fcb-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="01fcb-135">Si *pSrcResource* contient un effet de texte, Flags peut être une combinaison d' [indicateurs D3DXSHADER](d3dxshader-flags.md) et d’indicateurs [D3DXFX](d3dxfx.md) ; Sinon, *pSrcResource* contient un effet binaire et les seuls indicateurs honorés sont des indicateurs D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="01fcb-135">If *pSrcResource* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcResource* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="01fcb-136">Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="01fcb-136">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="01fcb-137">Pour plus d’informations [, consultez outil de compilateur Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="01fcb-137">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="01fcb-138">*pPool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01fcb-138">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01fcb-139">Type : **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="01fcb-139">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="01fcb-140">Pointeur vers un objet [**ID3DXEffectPool**](id3dxeffectpool.md) à utiliser pour les paramètres partagés.</span><span class="sxs-lookup"><span data-stu-id="01fcb-140">Pointer to an [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="01fcb-141">Si cette valeur est **null**, aucun paramètre n’est partagé.</span><span class="sxs-lookup"><span data-stu-id="01fcb-141">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="01fcb-142">*ppEffect* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="01fcb-142">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01fcb-143">Type : **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="01fcb-143">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="01fcb-144">Retourne une mémoire tampon contenant l’effet compilé.</span><span class="sxs-lookup"><span data-stu-id="01fcb-144">Returns a buffer containing the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="01fcb-145">*ppCompilationErrors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="01fcb-145">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01fcb-146">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="01fcb-146">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="01fcb-147">Retourne une mémoire tampon qui contient une liste d’erreurs de compilation.</span><span class="sxs-lookup"><span data-stu-id="01fcb-147">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01fcb-148">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01fcb-148">Return value</span></span>

<span data-ttu-id="01fcb-149">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="01fcb-149">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="01fcb-150">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="01fcb-150">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="01fcb-151">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="01fcb-151">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="01fcb-152">Notes</span><span class="sxs-lookup"><span data-stu-id="01fcb-152">Remarks</span></span>

<span data-ttu-id="01fcb-153">Cette fonction est une version étendue de [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) qui permet à une application de spécifier les constantes d’effet qui seront gérées par l’application.</span><span class="sxs-lookup"><span data-stu-id="01fcb-153">This function is an extended version of [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="01fcb-154">Une constante gérée par l’application est ignorée par le système d’effets.</span><span class="sxs-lookup"><span data-stu-id="01fcb-154">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="01fcb-155">Autrement dit, l’application est responsable de l’initialisation de la constante, ainsi que de l’enregistrement et de la restauration de son état chaque fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="01fcb-155">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="01fcb-156">Cette fonction vérifie chaque constante dans pSkipConstants pour voir ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="01fcb-156">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="01fcb-157">Elle est liée à un registre de constantes.</span><span class="sxs-lookup"><span data-stu-id="01fcb-157">It is bound to a constant register.</span></span>
-   <span data-ttu-id="01fcb-158">Il est utilisé uniquement dans le code de nuanceur HLSL.</span><span class="sxs-lookup"><span data-stu-id="01fcb-158">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="01fcb-159">Si une constante est nommée dans la chaîne qui n’est pas présente dans l’effet, elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="01fcb-159">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

<span data-ttu-id="01fcb-160">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="01fcb-160">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="01fcb-161">Dans le cas contraire, le type de données LPCTSTR est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="01fcb-161">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="01fcb-162">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="01fcb-162">The compiler setting also determines the function version.</span></span> <span data-ttu-id="01fcb-163">Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateEffectFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="01fcb-163">If Unicode is defined, the function call resolves to D3DXCreateEffectFromResourceW.</span></span> <span data-ttu-id="01fcb-164">Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateEffectFromResourceA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="01fcb-164">Otherwise, the function call resolves to D3DXCreateEffectFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="01fcb-165">D3DXCreateEffectFromResource charge des données à partir d’une ressource de type RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="01fcb-165">D3DXCreateEffectFromResource loads data from a resource of type RT\_RCDATA.</span></span> <span data-ttu-id="01fcb-166">Pour plus d’informations sur les ressources Windows, consultez MSDN.</span><span class="sxs-lookup"><span data-stu-id="01fcb-166">See MSDN for more information about Windows resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="01fcb-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01fcb-167">Requirements</span></span>



| <span data-ttu-id="01fcb-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01fcb-168">Requirement</span></span> | <span data-ttu-id="01fcb-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="01fcb-169">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="01fcb-170">En-tête</span><span class="sxs-lookup"><span data-stu-id="01fcb-170">Header</span></span><br/>  | <dl> <span data-ttu-id="01fcb-171"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="01fcb-171"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="01fcb-172">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="01fcb-172">Library</span></span><br/> | <dl> <span data-ttu-id="01fcb-173"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01fcb-173"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="01fcb-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01fcb-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01fcb-175">Fonctions Effect</span><span class="sxs-lookup"><span data-stu-id="01fcb-175">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="01fcb-176">**D3DXCreateEffectEx**</span><span class="sxs-lookup"><span data-stu-id="01fcb-176">**D3DXCreateEffectEx**</span></span>](d3dxcreateeffectex.md)
</dt> <dt>

[<span data-ttu-id="01fcb-177">**D3DXCreateEffectFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="01fcb-177">**D3DXCreateEffectFromFileEx**</span></span>](d3dxcreateeffectfromfileex.md)
</dt> </dl>

 

 
