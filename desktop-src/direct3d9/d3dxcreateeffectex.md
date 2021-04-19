---
description: Crée un effet à partir d’une description d’effet ASCII ou binaire. Cette fonction est une version étendue de D3DXCreateEffect qui permet à une application de contrôler les paramètres qui sont ignorés par le système d’effets.
ms.assetid: b08f727e-6061-4e78-8243-08c4ccab342d
title: D3DXCreateEffectEx, fonction (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 979b09f852e692b4c25414607f79cd8792342755
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538520"
---
# <a name="d3dxcreateeffectex-function"></a><span data-ttu-id="238a7-104">D3DXCreateEffectEx fonction)</span><span class="sxs-lookup"><span data-stu-id="238a7-104">D3DXCreateEffectEx function</span></span>

<span data-ttu-id="238a7-105">Crée un effet à partir d’une description d’effet ASCII ou binaire.</span><span class="sxs-lookup"><span data-stu-id="238a7-105">Creates an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="238a7-106">Cette fonction est une version étendue de [**D3DXCreateEffect**](d3dxcreateeffect.md) qui permet à une application de contrôler les paramètres qui sont ignorés par le système d’effets.</span><span class="sxs-lookup"><span data-stu-id="238a7-106">This function is an extended version of [**D3DXCreateEffect**](d3dxcreateeffect.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="238a7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="238a7-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="238a7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="238a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="238a7-109">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="238a7-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="238a7-110">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="238a7-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="238a7-111">Pointeur vers l’appareil qui va créer l’effet.</span><span class="sxs-lookup"><span data-stu-id="238a7-111">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="238a7-112">Consultez [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="238a7-112">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="238a7-113">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="238a7-113">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="238a7-114">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="238a7-114">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="238a7-115">Pointeur vers une mémoire tampon qui contient une description d’effet.</span><span class="sxs-lookup"><span data-stu-id="238a7-115">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="238a7-116">*SrcDataLen* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="238a7-116">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="238a7-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="238a7-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="238a7-118">Longueur des données d’effet, en octets.</span><span class="sxs-lookup"><span data-stu-id="238a7-118">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="238a7-119">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="238a7-119">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="238a7-120">Type : **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="238a7-120">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="238a7-121">Tableau de structures [**D3DXMACRO**](d3dxmacro.md) se terminant par un caractère **null** facultatif qui décrivent les définitions de préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="238a7-121">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="238a7-122">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="238a7-122">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="238a7-123">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="238a7-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="238a7-124">Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="238a7-124">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="238a7-125">Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include.</span><span class="sxs-lookup"><span data-stu-id="238a7-125">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="238a7-126">Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.</span><span class="sxs-lookup"><span data-stu-id="238a7-126">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="238a7-127">*pSkipConstants* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="238a7-127">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="238a7-128">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="238a7-128">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="238a7-129">Chaîne de paramètres d’effet qui sera ignorée par le système d’effet.</span><span class="sxs-lookup"><span data-stu-id="238a7-129">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="238a7-130">La chaîne doit se terminer par une **valeur null** et doit contenir le nom de chaque constante gérée par l’application, séparées par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="238a7-130">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="238a7-131">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="238a7-131">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="238a7-132">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="238a7-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="238a7-133">Si *pSrcData* contient un effet de texte, Flags peut être une combinaison d' [indicateurs D3DXSHADER](d3dxshader-flags.md) et d’indicateurs [D3DXFX](d3dxfx.md) ; Sinon, *pSrcData* contient un effet binaire et les seuls indicateurs honorés sont des indicateurs D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="238a7-133">If *pSrcData* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcData* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="238a7-134">Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="238a7-134">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="238a7-135">Pour plus d’informations [, consultez outil de compilateur Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="238a7-135">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="238a7-136">*pPool* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="238a7-136">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="238a7-137">Type : **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="238a7-137">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="238a7-138">Pointeur vers un objet [**ID3DXEffectPool**](id3dxeffectpool.md) à utiliser pour les paramètres partagés.</span><span class="sxs-lookup"><span data-stu-id="238a7-138">Pointer to an [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="238a7-139">Si cette valeur est **null**, aucun paramètre n’est partagé.</span><span class="sxs-lookup"><span data-stu-id="238a7-139">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="238a7-140">*ppEffect* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="238a7-140">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="238a7-141">Type : **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="238a7-141">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="238a7-142">Retourne un pointeur vers une interface [**ID3DXEffect**](id3dxeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="238a7-142">Returns a pointer to an [**ID3DXEffect**](id3dxeffect.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="238a7-143">*ppCompilationErrors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="238a7-143">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="238a7-144">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="238a7-144">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="238a7-145">Retourne une mémoire tampon qui contient une liste d’erreurs de compilation.</span><span class="sxs-lookup"><span data-stu-id="238a7-145">Returns a buffer containing a list of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="238a7-146">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="238a7-146">Return value</span></span>

<span data-ttu-id="238a7-147">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="238a7-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="238a7-148">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="238a7-148">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="238a7-149">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="238a7-149">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="238a7-150">Notes</span><span class="sxs-lookup"><span data-stu-id="238a7-150">Remarks</span></span>

<span data-ttu-id="238a7-151">Cette fonction est une version étendue de [**D3DXCreateEffect**](d3dxcreateeffect.md) qui permet à une application de spécifier les constantes d’effet qui seront gérées par l’application.</span><span class="sxs-lookup"><span data-stu-id="238a7-151">This function is an extended version of [**D3DXCreateEffect**](d3dxcreateeffect.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="238a7-152">Une constante gérée par l’application est ignorée par le système d’effets.</span><span class="sxs-lookup"><span data-stu-id="238a7-152">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="238a7-153">Autrement dit, l’application est responsable de l’initialisation de la constante, ainsi que de l’enregistrement et de la restauration de son état chaque fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="238a7-153">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="238a7-154">Cette fonction vérifie chaque constante dans pSkipConstants pour voir ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="238a7-154">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="238a7-155">Elle est liée à un registre de constantes.</span><span class="sxs-lookup"><span data-stu-id="238a7-155">It is bound to a constant register.</span></span>
-   <span data-ttu-id="238a7-156">Il est utilisé uniquement dans le code de nuanceur HLSL.</span><span class="sxs-lookup"><span data-stu-id="238a7-156">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="238a7-157">Si une constante est nommée dans la chaîne qui n’est pas présente dans l’effet, elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="238a7-157">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="238a7-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="238a7-158">Requirements</span></span>



| <span data-ttu-id="238a7-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="238a7-159">Requirement</span></span> | <span data-ttu-id="238a7-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="238a7-160">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="238a7-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="238a7-161">Header</span></span><br/>  | <dl> <span data-ttu-id="238a7-162"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="238a7-162"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="238a7-163">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="238a7-163">Library</span></span><br/> | <dl> <span data-ttu-id="238a7-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="238a7-164"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="238a7-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="238a7-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="238a7-166">Fonctions Effect</span><span class="sxs-lookup"><span data-stu-id="238a7-166">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="238a7-167">**D3DXCreateEffectFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="238a7-167">**D3DXCreateEffectFromFileEx**</span></span>](d3dxcreateeffectfromfileex.md)
</dt> <dt>

[<span data-ttu-id="238a7-168">**D3DXCreateEffectFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="238a7-168">**D3DXCreateEffectFromResourceEx**</span></span>](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
