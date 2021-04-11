---
description: Rééchantillonne une texture dans le paramétrage de ce gutterhelper.
ms.assetid: a5ace0e4-2e89-471b-bdfb-67d5e85c6f46
title: 'ID3DXTextureGutterHelper :: ResampleTex, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ResampleTex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ad8b4cefe0b368cbf81de4ddc030f32cda8fb17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211880"
---
# <a name="id3dxtexturegutterhelperresampletex-method"></a><span data-ttu-id="86cea-103">ID3DXTextureGutterHelper :: ResampleTex, méthode</span><span class="sxs-lookup"><span data-stu-id="86cea-103">ID3DXTextureGutterHelper::ResampleTex method</span></span>

<span data-ttu-id="86cea-104">Rééchantillonne une texture dans le paramétrage de ce gutterhelper.</span><span class="sxs-lookup"><span data-stu-id="86cea-104">Resamples a texture into this gutterhelper's parameterization.</span></span>

## <a name="syntax"></a><span data-ttu-id="86cea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86cea-105">Syntax</span></span>


```C++
HRESULT ResampleTex(
  [in]  LPDIRECT3DTEXTURE9 pTextureIn,
  [in]  LPD3DXMESH         pMeshIn,
  [in]  D3DDECLUSAGE       Usage,
  [in]  UINT               UsageIndex,
  [out] LPDIRECT3DTEXTURE9 pTextureOut
);
```



## <a name="parameters"></a><span data-ttu-id="86cea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86cea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86cea-107">*pTextureIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="86cea-107">*pTextureIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86cea-108">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="86cea-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="86cea-109">Texture qui correspond au paramétrage d’origine dans pMeshIn.</span><span class="sxs-lookup"><span data-stu-id="86cea-109">Texture that corresponds to the original parameterization in pMeshIn.</span></span> <span data-ttu-id="86cea-110">Cette texture sera utilisée pour créer pTextureOut.</span><span class="sxs-lookup"><span data-stu-id="86cea-110">This texture will be used to create pTextureOut.</span></span>

</dd> <dt>

<span data-ttu-id="86cea-111">*pMeshIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="86cea-111">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86cea-112">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="86cea-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="86cea-113">Maille contenant les paramétrages originaux et nouveaux.</span><span class="sxs-lookup"><span data-stu-id="86cea-113">Mesh containing the original and new parameterizations.</span></span> <span data-ttu-id="86cea-114">Il est nécessaire pour stocker le nouveau paramétrage dans l' \_ index 0 D3DDECLUSAGE texcoord.</span><span class="sxs-lookup"><span data-stu-id="86cea-114">It is required to store the new parameterization in D3DDECLUSAGE\_TEXCOORD index 0.</span></span>

</dd> <dt>

<span data-ttu-id="86cea-115">*Utilisation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="86cea-115">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86cea-116">Type : **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="86cea-116">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="86cea-117">Utilisation des données de vertex (utilisée en association avec UsageIndex) qui identifie le composant de la déclaration de vertex qui contient le paramétrage d’origine dans pMeshIn.</span><span class="sxs-lookup"><span data-stu-id="86cea-117">Vertex data usage (used in combination with UsageIndex) which identifies the component of the vertex declaration that contains the original parameterization in pMeshIn.</span></span> <span data-ttu-id="86cea-118">Consultez [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="86cea-118">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="86cea-119">*UsageIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="86cea-119">*UsageIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86cea-120">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="86cea-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="86cea-121">Index de base zéro (utilisé en association avec l’utilisation), qui identifie le composant de la déclaration de vertex qui contient le paramétrage d’origine dans pMeshIn.</span><span class="sxs-lookup"><span data-stu-id="86cea-121">Zero-based index (used in combination with Usage), which identifies the component of the vertex declaration that contains the original parameterization in pMeshIn.</span></span> <span data-ttu-id="86cea-122">La combinaison de D3DDECLUSAGE \_ texcoord et de l’index 0 est requise pour le nouveau paramétrage ; toute autre combinaison d’utilisation/d’index peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="86cea-122">The combination of D3DDECLUSAGE\_TEXCOORD and index 0 is required for the new parameterization; any other usage/index combination may be used.</span></span>

</dd> <dt>

<span data-ttu-id="86cea-123">*pTextureOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="86cea-123">*pTextureOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86cea-124">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="86cea-124">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="86cea-125">Texture rééchantillonnée.</span><span class="sxs-lookup"><span data-stu-id="86cea-125">Resampled texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86cea-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86cea-126">Return value</span></span>

<span data-ttu-id="86cea-127">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="86cea-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="86cea-128">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="86cea-128">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="86cea-129">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="86cea-129">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="86cea-130">Notes</span><span class="sxs-lookup"><span data-stu-id="86cea-130">Remarks</span></span>

<span data-ttu-id="86cea-131">Un paramétrage dans le cas de cette fonction est un ensemble de coordonnées de texture qui mappe les triangles d’une maille aux triangles d’une texture.</span><span class="sxs-lookup"><span data-stu-id="86cea-131">A parameterization in the case of this function is a set of texture coordinates that maps the triangles of a mesh to the triangles on a texture.</span></span> <span data-ttu-id="86cea-132">Le nouveau paramétrage est l’ensemble des coordonnées de texture contenues dans l’interface d’assistance de reliure, et le paramétrage d’origine est l’ensemble des coordonnées de texture contenues dans le maillage d’entrée.</span><span class="sxs-lookup"><span data-stu-id="86cea-132">The new parameterization is the set of texture coordinates contained in the gutter helper interface, and the original parameterization is the set of texture coordinates contained within the input mesh.</span></span>

<span data-ttu-id="86cea-133">Il est supposé que les coordonnées de texture sont comprises entre 0 et 1 (inclus), et le nouveau paramétrage doit être déclaré dans la déclaration de vertex comme index de coordonnée de texture 0.</span><span class="sxs-lookup"><span data-stu-id="86cea-133">It is assumed that texture coordinates are between 0 and 1, inclusive, and the new parameterization must be declared in the vertex declaration as texture coordinate index 0.</span></span> <span data-ttu-id="86cea-134">La texture d’origine et la texture rééchantillonnée doivent avoir la même largeur et la même hauteur.</span><span class="sxs-lookup"><span data-stu-id="86cea-134">The original texture and the resampled texture must have the same width and height.</span></span>

<span data-ttu-id="86cea-135">Par exemple, pour préparer le rééchantillonnage d’une texture :</span><span class="sxs-lookup"><span data-stu-id="86cea-135">For example, to prepare for resampling a texture:</span></span>

-   <span data-ttu-id="86cea-136">Créez l’interface de texture d’origine (pOriginalTex ci-dessous) à l’aide d’une fonction comme [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="86cea-136">Create the original texture interface (pOriginalTex below) using a function like [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span></span>
-   <span data-ttu-id="86cea-137">Créez la nouvelle interface de texture pour la texture rééchantillonnée (pResampledTex ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="86cea-137">Create the new texture interface for the resampled texture (pResampledTex below).</span></span> <span data-ttu-id="86cea-138">La taille de cette texture doit correspondre à la taille (largeur et hauteur) de la texture d’assistance de la reliure.</span><span class="sxs-lookup"><span data-stu-id="86cea-138">The size of this texture must match the size (width and height) of the gutter helper texture.</span></span>
-   <span data-ttu-id="86cea-139">Appelez [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) pour obtenir le nouveau paramétrage comme indiqué ici :</span><span class="sxs-lookup"><span data-stu-id="86cea-139">Call [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) to obtain the new parameterization as shown here:</span></span>


```
// Given:
// pMesh points to a mesh that contains the original and new texture coordinates
ID3DXTextureGutterHelper * pGutterHelper;
    
// Mesh vertex declaration
D3DVERTEXELEMENT9 decl[] = {
    {0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0},
    // contains new set of texcoords
    {0, 24, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0}, 
    // contains original set of texcoords
    {0, 32, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1}, 
    D3DDECL_END()
};
    
// Create a gutter helper with the new parameterization
hr = D3DXCreateTextureGutterHelper(width, height, pMesh, 1, &pGutterHelper);  
    
// Resample the texture
hr = pGutterHelper->ResampleTex(pOriginalTex, pMesh, D3DDECLUSAGE_TEXCOORD, 
           1, pResampledTex); 
    
// Release the gutter helper interface when done with it
```



<span data-ttu-id="86cea-140">Un scénario courant consiste à utiliser UVAtlas pour créer un Atlas de textures, puis à utiliser ResampleTex pour rééchantillonner la texture dans le nouveau paramétrage.</span><span class="sxs-lookup"><span data-stu-id="86cea-140">One common scenario might be to use UVAtlas to create a texture atlas and then use ResampleTex to resample the texture into the new parameterization.</span></span> <span data-ttu-id="86cea-141">Pour plus d’informations sur les Atlas, consultez [utilisation de UVAtlas (Direct3D 9)](using-uvatlas.md).</span><span class="sxs-lookup"><span data-stu-id="86cea-141">For more information about atlases, see [Using UVAtlas (Direct3D 9)](using-uvatlas.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86cea-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86cea-142">Requirements</span></span>



| <span data-ttu-id="86cea-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86cea-143">Requirement</span></span> | <span data-ttu-id="86cea-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="86cea-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86cea-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="86cea-145">Header</span></span><br/>  | <dl> <span data-ttu-id="86cea-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="86cea-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="86cea-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="86cea-147">Library</span></span><br/> | <dl> <span data-ttu-id="86cea-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86cea-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="86cea-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86cea-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86cea-150">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="86cea-150">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> <dt>

[<span data-ttu-id="86cea-151">**D3DXUVAtlasCreate**</span><span class="sxs-lookup"><span data-stu-id="86cea-151">**D3DXUVAtlasCreate**</span></span>](d3dxuvatlascreate.md)
</dt> </dl>

 

 
