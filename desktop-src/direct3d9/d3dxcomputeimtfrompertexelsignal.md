---
description: Calcule les IMT par triangle à partir des données par texture. Cette fonction est similaire à D3DXComputeIMTFromTexture, mais elle utilise un tableau de valeurs float pour transmettre les données, et elle peut calculer des valeurs dimensionnelles supérieures à 4.
ms.assetid: 4a151184-e67e-41e9-83c6-63da72f262fa
title: D3DXComputeIMTFromPerTexelSignal, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerTexelSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3db71fbc931f7bdb3e73c8d949a163607e66c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523196"
---
# <a name="d3dxcomputeimtfrompertexelsignal-function"></a><span data-ttu-id="dc788-104">D3DXComputeIMTFromPerTexelSignal fonction)</span><span class="sxs-lookup"><span data-stu-id="dc788-104">D3DXComputeIMTFromPerTexelSignal function</span></span>

<span data-ttu-id="dc788-105">Calcule les IMT par triangle à partir des données par texture.</span><span class="sxs-lookup"><span data-stu-id="dc788-105">Calculate per-triangle IMT's from per-texel data.</span></span> <span data-ttu-id="dc788-106">Cette fonction est similaire à [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md), mais elle utilise un tableau de valeurs float pour transmettre les données, et elle peut calculer des valeurs dimensionnelles supérieures à 4.</span><span class="sxs-lookup"><span data-stu-id="dc788-106">This function is similar to [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md), but it uses a float array to pass in the data, and it can calculate higher dimensional values than 4.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc788-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc788-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromPerTexelSignal(
  _In_  LPD3DXMESH      pMesh,
  _In_  DWORD           dwTextureIndex,
  _In_  FLOAT           *pfTexelSignal,
  _In_  UINT            uWidth,
  _In_  UINT            uHeight,
  _In_  UINT            uSignalDimension,
  _In_  UINT            uComponents,
  _In_  DWORD           dwOptions,
        LPD3DXUVATLASCB pStatusCallback,
        LPVOID          pUserContext,
  _Out_ LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="dc788-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc788-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc788-109">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc788-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc788-110">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="dc788-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="dc788-111">Pointeur vers un maillage d’entrée (voir [**ID3DXMesh**](id3dxmesh.md)) qui contient la géométrie d’objet pour le calcul du IMT.</span><span class="sxs-lookup"><span data-stu-id="dc788-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="dc788-112">*dwTextureIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc788-112">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc788-113">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc788-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc788-114">Index de coordonnées de texture de base zéro qui identifie le jeu de coordonnées de texture à utiliser.</span><span class="sxs-lookup"><span data-stu-id="dc788-114">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="dc788-115">*pfTexelSignal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc788-115">*pfTexelSignal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc788-116">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc788-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dc788-117">Pointeur vers un tableau de texels d’entrée à partir duquel IMT sera calculé.</span><span class="sxs-lookup"><span data-stu-id="dc788-117">A pointer to an array of input texels from which IMT will be computed.</span></span> <span data-ttu-id="dc788-118">La taille du tableau est uWidth \* uHeight \* uComponents.</span><span class="sxs-lookup"><span data-stu-id="dc788-118">The array size is uWidth\*uHeight\*uComponents.</span></span>

</dd> <dt>

<span data-ttu-id="dc788-119">*uWidth* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc788-119">*uWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc788-120">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc788-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc788-121">Largeur de la texture en pixels.</span><span class="sxs-lookup"><span data-stu-id="dc788-121">Texture width in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="dc788-122">*uHeight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc788-122">*uHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc788-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc788-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc788-124">Hauteur de la texture en pixels.</span><span class="sxs-lookup"><span data-stu-id="dc788-124">Texture height in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="dc788-125">*uSignalDimension* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc788-125">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc788-126">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc788-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc788-127">Nombre de valeurs float par composant dans chaque élément du tableau de signal.</span><span class="sxs-lookup"><span data-stu-id="dc788-127">The number of floats per-component in each element of the signal array.</span></span>

</dd> <dt>

<span data-ttu-id="dc788-128">*uComponents* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc788-128">*uComponents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc788-129">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc788-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc788-130">Nombre de composants dans chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="dc788-130">The number of components in each texel.</span></span>

</dd> <dt>

<span data-ttu-id="dc788-131">*dwOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc788-131">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc788-132">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc788-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc788-133">Options de retour à la ligne.</span><span class="sxs-lookup"><span data-stu-id="dc788-133">Texture wrap options.</span></span> <span data-ttu-id="dc788-134">Il s’agit d’une combinaison d’un ou plusieurs [**indicateurs D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="dc788-134">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc788-135">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="dc788-135">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="dc788-136">Type : **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="dc788-136">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="dc788-137">Pointeur vers une fonction de rappel pour surveiller la progression du calcul IMT.</span><span class="sxs-lookup"><span data-stu-id="dc788-137">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="dc788-138">*pUserContext*</span><span class="sxs-lookup"><span data-stu-id="dc788-138">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="dc788-139">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc788-139">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc788-140">Pointeur vers une variable définie par l’utilisateur qui est passée à la fonction de rappel d’État.</span><span class="sxs-lookup"><span data-stu-id="dc788-140">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="dc788-141">Généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="dc788-141">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="dc788-142">*ppIMTData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dc788-142">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc788-143">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc788-143">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="dc788-144">Pointeur vers la mémoire tampon (consultez [**ID3DXBuffer**](id3dxbuffer.md)) contenant le tableau IMT retourné.</span><span class="sxs-lookup"><span data-stu-id="dc788-144">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="dc788-145">Ce tableau peut être fourni comme entrée aux fonctions D3DX [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) pour classer par ordre de priorité l’allocation d’espace de texture dans le paramétrage de la texture.</span><span class="sxs-lookup"><span data-stu-id="dc788-145">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc788-146">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc788-146">Return value</span></span>

<span data-ttu-id="dc788-147">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dc788-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dc788-148">Si la fonction est réussie, la valeur de retour est D3D \_ OK ; sinon, la valeur est D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="dc788-148">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc788-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc788-149">Requirements</span></span>



| <span data-ttu-id="dc788-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc788-150">Requirement</span></span> | <span data-ttu-id="dc788-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc788-151">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc788-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc788-152">Header</span></span><br/>  | <dl> <span data-ttu-id="dc788-153"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc788-153"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dc788-154">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dc788-154">Library</span></span><br/> | <dl> <span data-ttu-id="dc788-155"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc788-155"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dc788-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc788-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc788-157">UVAtlas, fonctions</span><span class="sxs-lookup"><span data-stu-id="dc788-157">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="dc788-158">Utilisation de UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dc788-158">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
