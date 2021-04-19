---
description: Définit les paramètres de déplacement de la géométrie du maillage.
ms.assetid: 4c78e5b3-fb63-4341-a811-5531cf9564e7
title: 'ID3DXPatchMesh :: SetDisplaceParam, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.SetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1d59791859e0330415512db1551709729455d0d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524869"
---
# <a name="id3dxpatchmeshsetdisplaceparam-method"></a><span data-ttu-id="c5fe8-103">ID3DXPatchMesh :: SetDisplaceParam, méthode</span><span class="sxs-lookup"><span data-stu-id="c5fe8-103">ID3DXPatchMesh::SetDisplaceParam method</span></span>

<span data-ttu-id="c5fe8-104">Définit les paramètres de déplacement de la géométrie du maillage.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-104">Sets mesh geometry displacement parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5fe8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5fe8-105">Syntax</span></span>


```C++
HRESULT SetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 Texture,
  [in] D3DTEXTUREFILTERTYPE   MinFilter,
  [in] D3DTEXTUREFILTERTYPE   MagFilter,
  [in] D3DTEXTUREFILTERTYPE   MipFilter,
  [in] D3DTEXTUREADDRESS      Wrap,
  [in] DWORD                  dwLODBias
);
```



## <a name="parameters"></a><span data-ttu-id="c5fe8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5fe8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5fe8-107">*Texture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c5fe8-107">*Texture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5fe8-108">Type : **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-108">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="c5fe8-109">Texture contenant les données de déplacement.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-109">Texture containing the displacement data.</span></span>

</dd> <dt>

<span data-ttu-id="c5fe8-110">*MinFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c5fe8-110">*MinFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5fe8-111">Type : **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-111">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span></span>

<span data-ttu-id="c5fe8-112">Niveau de minimisation.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-112">Minification level.</span></span> <span data-ttu-id="c5fe8-113">Pour plus d’informations, consultez [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="c5fe8-113">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5fe8-114">*MagFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c5fe8-114">*MagFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5fe8-115">Type : **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-115">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span></span>

<span data-ttu-id="c5fe8-116">Niveau d’agrandissement.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-116">Magnification level.</span></span> <span data-ttu-id="c5fe8-117">Pour plus d’informations, consultez [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="c5fe8-117">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5fe8-118">*MipFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c5fe8-118">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5fe8-119">Type : **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-119">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span></span>

<span data-ttu-id="c5fe8-120">Niveau de filtre MIP.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-120">Mip filter level.</span></span> <span data-ttu-id="c5fe8-121">Pour plus d’informations, consultez [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="c5fe8-121">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5fe8-122">*Retour à la ligne* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c5fe8-122">*Wrap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5fe8-123">Type : **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-123">Type: **[**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)**</span></span>

<span data-ttu-id="c5fe8-124">Mode de retour à la ligne de l’adresse de texture.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-124">Texture address wrap mode.</span></span> <span data-ttu-id="c5fe8-125">Pour plus d’informations, consultez [ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)</span><span class="sxs-lookup"><span data-stu-id="c5fe8-125">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)</span></span>

</dd> <dt>

<span data-ttu-id="c5fe8-126">*dwLODBias* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c5fe8-126">*dwLODBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5fe8-127">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5fe8-128">Niveau de la valeur de décalage des détails.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-128">Level of detail bias value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5fe8-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5fe8-129">Return value</span></span>

<span data-ttu-id="c5fe8-130">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5fe8-131">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-131">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c5fe8-132">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-132">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5fe8-133">Notes</span><span class="sxs-lookup"><span data-stu-id="c5fe8-133">Remarks</span></span>

<span data-ttu-id="c5fe8-134">Les mappages de déplacement ne peuvent être que des textures 2D.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-134">Displacement maps can only be 2D textures.</span></span> <span data-ttu-id="c5fe8-135">Mappage MIP est ignoré pour le pavage non adaptatif.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-135">Mipmapping is ignored for nonadaptive tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5fe8-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5fe8-136">Requirements</span></span>



| <span data-ttu-id="c5fe8-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5fe8-137">Requirement</span></span> | <span data-ttu-id="c5fe8-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5fe8-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5fe8-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5fe8-139">Header</span></span><br/>  | <dl> <span data-ttu-id="c5fe8-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5fe8-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c5fe8-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c5fe8-141">Library</span></span><br/> | <dl> <span data-ttu-id="c5fe8-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5fe8-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c5fe8-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5fe8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5fe8-144">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="c5fe8-144">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
