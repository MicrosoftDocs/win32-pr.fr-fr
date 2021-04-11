---
description: Utilise un système de coordonnées droitier pour créer un maillage contenant une sphère.
ms.assetid: d3198805-9435-4849-892d-ec98dc2221d2
title: D3DXCreateSphere, fonction (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56ac6b8e8cc2195e2176e505cf430ea33b6b6ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211772"
---
# <a name="d3dxcreatesphere-function"></a><span data-ttu-id="35114-103">D3DXCreateSphere fonction)</span><span class="sxs-lookup"><span data-stu-id="35114-103">D3DXCreateSphere function</span></span>

<span data-ttu-id="35114-104">Utilise un système de coordonnées droitier pour créer un maillage contenant une sphère.</span><span class="sxs-lookup"><span data-stu-id="35114-104">Uses a left-handed coordinate system to create a mesh containing a sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="35114-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35114-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSphere(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="35114-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35114-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35114-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35114-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35114-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="35114-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="35114-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé au maillage de sphère créé.</span><span class="sxs-lookup"><span data-stu-id="35114-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created sphere mesh.</span></span>

</dd> <dt>

<span data-ttu-id="35114-110">*Rayon* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35114-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35114-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35114-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35114-112">Rayon de la sphère.</span><span class="sxs-lookup"><span data-stu-id="35114-112">Radius of the sphere.</span></span> <span data-ttu-id="35114-113">Cette valeur doit être supérieure ou égale à 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="35114-113">This value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="35114-114">*Tranches* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35114-114">*Slices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35114-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35114-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35114-116">Nombre de tranches relatives à l’axe principal.</span><span class="sxs-lookup"><span data-stu-id="35114-116">Number of slices about the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="35114-117">*Piles* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35114-117">*Stacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35114-118">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35114-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35114-119">Nombre de piles le long de l’axe principal.</span><span class="sxs-lookup"><span data-stu-id="35114-119">Number of stacks along the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="35114-120">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="35114-120">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35114-121">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="35114-121">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="35114-122">Adresse d’un pointeur vers la forme de sortie, une interface [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="35114-122">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="35114-123">*ppAdjacency* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="35114-123">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35114-124">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="35114-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="35114-125">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="35114-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="35114-126">Quand la méthode est retournée, ce paramètre est rempli avec un tableau de trois DWORDs par visage qui spécifient les trois voisins pour chaque visage de la maille.</span><span class="sxs-lookup"><span data-stu-id="35114-126">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="35114-127">La **valeur null** peut être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="35114-127">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35114-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35114-128">Return value</span></span>

<span data-ttu-id="35114-129">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="35114-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="35114-130">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="35114-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="35114-131">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="35114-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="35114-132">Notes</span><span class="sxs-lookup"><span data-stu-id="35114-132">Remarks</span></span>

<span data-ttu-id="35114-133">La sphère créée est centrée à l’origine et son axe est aligné avec l’axe z.</span><span class="sxs-lookup"><span data-stu-id="35114-133">The created sphere is centered at the origin, and its axis is aligned with the z-axis.</span></span>

<span data-ttu-id="35114-134">Cette fonction crée une maille avec l' \_ option de création managée D3DXMESH et [D3DFVF \_ xyz \| D3DFVF \_ ](d3dfvf.md) le format de vertex flexible normal.</span><span class="sxs-lookup"><span data-stu-id="35114-134">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="35114-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35114-135">Requirements</span></span>



| <span data-ttu-id="35114-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35114-136">Requirement</span></span> | <span data-ttu-id="35114-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="35114-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35114-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="35114-138">Header</span></span><br/>  | <dl> <span data-ttu-id="35114-139"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="35114-139"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="35114-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="35114-140">Library</span></span><br/> | <dl> <span data-ttu-id="35114-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35114-141"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="35114-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35114-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35114-143">Fonctions de dessin de forme</span><span class="sxs-lookup"><span data-stu-id="35114-143">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
