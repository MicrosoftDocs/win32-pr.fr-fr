---
description: Calcule les IMT par triangle à partir d’une texture mappée sur un maillage, à utiliser éventuellement comme entrée pour les fonctions D3DX UVAtlas.
ms.assetid: 6671edc4-e494-4847-ae99-b9e56651a875
title: D3DXComputeIMTFromTexture, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2fbed0411f3562e3a05ec2ec4df99dfad6d8c902
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043154"
---
# <a name="d3dxcomputeimtfromtexture-function"></a><span data-ttu-id="fa336-103">D3DXComputeIMTFromTexture fonction)</span><span class="sxs-lookup"><span data-stu-id="fa336-103">D3DXComputeIMTFromTexture function</span></span>

<span data-ttu-id="fa336-104">Calcule les IMT par triangle à partir d’une texture mappée sur un maillage, à utiliser éventuellement comme entrée pour les fonctions D3DX [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md).</span><span class="sxs-lookup"><span data-stu-id="fa336-104">Calculates per-triangle IMT's from a texture mapped onto a mesh, to be used optionally as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fa336-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa336-105">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromTexture(
  _In_  LPD3DXMESH         pMesh,
  _In_  LPDIRECT3DTEXTURE9 pTexture,
  _In_  DWORD              dwTextureIndex,
  _In_  DWORD              dwOptions,
        LPD3DXUVATLASCB    pStatusCallback,
        LPVOID             pUserContext,
  _Out_ LPD3DXBUFFER       *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="fa336-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa336-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa336-107">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa336-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa336-108">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="fa336-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="fa336-109">Pointeur vers un maillage d’entrée (voir [**ID3DXMesh**](id3dxmesh.md)) qui contient la géométrie d’objet pour le calcul du IMT.</span><span class="sxs-lookup"><span data-stu-id="fa336-109">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="fa336-110">*pTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa336-110">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa336-111">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="fa336-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="fa336-112">Pointeur vers la texture (voir [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)) qui est mappée à la maille.</span><span class="sxs-lookup"><span data-stu-id="fa336-112">A pointer to the texture (see [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)) that is mapped to the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="fa336-113">*dwTextureIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa336-113">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa336-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa336-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fa336-115">Index de coordonnées de texture de base zéro qui identifie le jeu de coordonnées de texture à utiliser.</span><span class="sxs-lookup"><span data-stu-id="fa336-115">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="fa336-116">*dwOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa336-116">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa336-117">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa336-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fa336-118">Options de retour à la ligne.</span><span class="sxs-lookup"><span data-stu-id="fa336-118">Texture wrap options.</span></span> <span data-ttu-id="fa336-119">Il s’agit d’une combinaison d’un ou plusieurs [**indicateurs D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="fa336-119">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa336-120">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="fa336-120">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="fa336-121">Type : **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="fa336-121">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="fa336-122">Pointeur vers une fonction de rappel pour surveiller la progression du calcul IMT.</span><span class="sxs-lookup"><span data-stu-id="fa336-122">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="fa336-123">*pUserContext*</span><span class="sxs-lookup"><span data-stu-id="fa336-123">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="fa336-124">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fa336-124">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fa336-125">Pointeur vers une variable définie par l’utilisateur qui est passée à la fonction de rappel d’État.</span><span class="sxs-lookup"><span data-stu-id="fa336-125">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="fa336-126">Généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="fa336-126">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="fa336-127">*ppIMTData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fa336-127">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa336-128">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="fa336-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="fa336-129">Pointeur vers la mémoire tampon (consultez [**ID3DXBuffer**](id3dxbuffer.md)) contenant le tableau IMT retourné.</span><span class="sxs-lookup"><span data-stu-id="fa336-129">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="fa336-130">Ce tableau peut être fourni comme entrée aux fonctions D3DX [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) pour classer par ordre de priorité l’allocation d’espace de texture dans le paramétrage de la texture.</span><span class="sxs-lookup"><span data-stu-id="fa336-130">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa336-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa336-131">Return value</span></span>

<span data-ttu-id="fa336-132">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fa336-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fa336-133">Si la fonction est réussie, la valeur de retour est D3D \_ OK ; sinon, la valeur est D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fa336-133">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa336-134">Notes</span><span class="sxs-lookup"><span data-stu-id="fa336-134">Remarks</span></span>

<span data-ttu-id="fa336-135">À partir d’une texture qui est mappée sur la surface de la maille, l’algorithme calcule le IMT pour chaque visage.</span><span class="sxs-lookup"><span data-stu-id="fa336-135">Given a texture that maps over the surface of the mesh, the algorithm computes the IMT for each face.</span></span> <span data-ttu-id="fa336-136">Cela entraînera des triangles contenant des données de signal de faible fréquence pour occuper moins d’espace dans l’Atlas de texture final lorsqu’il est paramétré avec les fonctions UVAtlas.</span><span class="sxs-lookup"><span data-stu-id="fa336-136">This will cause triangles containing lower-frequency signal data to take up less space in the final texture atlas when parameterized with the UVAtlas functions.</span></span> <span data-ttu-id="fa336-137">La texture est supposée être interpolée sur la maille de manière bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="fa336-137">The texture is assumed to be interpolated over the mesh bilinearly.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa336-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa336-138">Requirements</span></span>



| <span data-ttu-id="fa336-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa336-139">Requirement</span></span> | <span data-ttu-id="fa336-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa336-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa336-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa336-141">Header</span></span><br/>  | <dl> <span data-ttu-id="fa336-142"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa336-142"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fa336-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fa336-143">Library</span></span><br/> | <dl> <span data-ttu-id="fa336-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa336-144"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fa336-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa336-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa336-146">UVAtlas, fonctions</span><span class="sxs-lookup"><span data-stu-id="fa336-146">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="fa336-147">Utilisation de UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fa336-147">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
