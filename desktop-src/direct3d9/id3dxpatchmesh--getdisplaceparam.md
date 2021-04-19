---
description: Obtient les paramètres de déplacement de la géométrie de maillage.
ms.assetid: 155724ba-71be-4e9f-8c84-bb04f8eec578
title: 'ID3DXPatchMesh :: GetDisplaceParam, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ce6891af8a15aa8f4af5c85312f124db6c05321
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538554"
---
# <a name="id3dxpatchmeshgetdisplaceparam-method"></a><span data-ttu-id="0b7b4-103">ID3DXPatchMesh :: GetDisplaceParam, méthode</span><span class="sxs-lookup"><span data-stu-id="0b7b4-103">ID3DXPatchMesh::GetDisplaceParam method</span></span>

<span data-ttu-id="0b7b4-104">Obtient les paramètres de déplacement de la géométrie de maillage.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-104">Gets mesh geometry displacement parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b7b4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b7b4-105">Syntax</span></span>


```C++
HRESULT GetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 *Texture,
  [in] D3DTEXTUREFILTERTYPE   *MinFilter,
  [in] D3DTEXTUREFILTERTYPE   *MagFilter,
  [in] D3DTEXTUREFILTERTYPE   *MipFilter,
  [in] D3DTEXTUREADDRESS      *Wrap,
  [in] DWORD                  *dwLODBias
);
```



## <a name="parameters"></a><span data-ttu-id="0b7b4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b7b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b7b4-107">*Texture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b7b4-107">*Texture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7b4-108">Type : **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="0b7b4-108">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span></span>

<span data-ttu-id="0b7b4-109">Texture contenant les données de déplacement.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-109">Texture containing the displacement data.</span></span>

</dd> <dt>

<span data-ttu-id="0b7b4-110">*MinFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b7b4-110">*MinFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7b4-111">Type : **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b7b4-111">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="0b7b4-112">Niveau de minimisation.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-112">Minification level.</span></span> <span data-ttu-id="0b7b4-113">Pour plus d’informations, consultez [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="0b7b4-113">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b7b4-114">*MagFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b7b4-114">*MagFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7b4-115">Type : **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b7b4-115">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="0b7b4-116">Niveau d’agrandissement.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-116">Magnification level.</span></span> <span data-ttu-id="0b7b4-117">Pour plus d’informations, consultez [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="0b7b4-117">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b7b4-118">*MipFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b7b4-118">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7b4-119">Type : **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b7b4-119">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="0b7b4-120">Niveau de filtre MIP.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-120">Mip filter level.</span></span> <span data-ttu-id="0b7b4-121">Pour plus d’informations, consultez [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="0b7b4-121">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b7b4-122">*Retour à la ligne* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b7b4-122">*Wrap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7b4-123">Type : **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b7b4-123">Type: **[**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***</span></span>

<span data-ttu-id="0b7b4-124">Mode de retour à la ligne de l’adresse de texture.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-124">Texture address wrap mode.</span></span> <span data-ttu-id="0b7b4-125">Pour plus d’informations, consultez [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="0b7b4-125">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b7b4-126">*dwLODBias* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b7b4-126">*dwLODBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b7b4-127">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0b7b4-127">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0b7b4-128">Niveau de la valeur de décalage des détails.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-128">Level of detail bias value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b7b4-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b7b4-129">Return value</span></span>

<span data-ttu-id="0b7b4-130">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b7b4-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b7b4-131">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-131">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0b7b4-132">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-132">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b7b4-133">Notes</span><span class="sxs-lookup"><span data-stu-id="0b7b4-133">Remarks</span></span>

<span data-ttu-id="0b7b4-134">Les mappages de déplacement ne peuvent être que des textures 2D.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-134">Displacement maps can only be 2D textures.</span></span> <span data-ttu-id="0b7b4-135">Mappage MIP est ignoré pour le pavage non adaptatif.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-135">Mipmapping is ignored for nonadaptive tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b7b4-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b7b4-136">Requirements</span></span>



| <span data-ttu-id="0b7b4-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b7b4-137">Requirement</span></span> | <span data-ttu-id="0b7b4-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b7b4-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b7b4-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b7b4-139">Header</span></span><br/>  | <dl> <span data-ttu-id="0b7b4-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b7b4-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0b7b4-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0b7b4-141">Library</span></span><br/> | <dl> <span data-ttu-id="0b7b4-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b7b4-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0b7b4-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b7b4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b7b4-144">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="0b7b4-144">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
