---
description: Utilise un système de coordonnées droitier pour créer une maille contenant un tore.
ms.assetid: 68df7650-8a87-4762-8b57-5704c419b0d7
title: D3DXCreateTorus, fonction (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTorus
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 384950ca1f00d0115135cf9ae36a2883ec5470e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211768"
---
# <a name="d3dxcreatetorus-function"></a><span data-ttu-id="5f941-103">D3DXCreateTorus fonction)</span><span class="sxs-lookup"><span data-stu-id="5f941-103">D3DXCreateTorus function</span></span>

<span data-ttu-id="5f941-104">Utilise un système de coordonnées droitier pour créer une maille contenant un tore.</span><span class="sxs-lookup"><span data-stu-id="5f941-104">Uses a left-handed coordinate system to create a mesh containing a torus.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f941-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f941-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTorus(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             InnerRadius,
  _In_  FLOAT             OuterRadius,
  _In_  UINT              Sides,
  _In_  UINT              Rings,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="5f941-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f941-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f941-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f941-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f941-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="5f941-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="5f941-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé au maillage de tores créé.</span><span class="sxs-lookup"><span data-stu-id="5f941-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created torus mesh.</span></span>

</dd> <dt>

<span data-ttu-id="5f941-110">*InnerRadius* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f941-110">*InnerRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f941-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f941-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5f941-112">Rayon interne du tore.</span><span class="sxs-lookup"><span data-stu-id="5f941-112">Inner-radius of the torus.</span></span> <span data-ttu-id="5f941-113">La valeur doit être supérieure ou égale à 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="5f941-113">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="5f941-114">*OuterRadius* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f941-114">*OuterRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f941-115">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f941-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5f941-116">Rayon externe du tore.</span><span class="sxs-lookup"><span data-stu-id="5f941-116">Outer-radius of the torus.</span></span> <span data-ttu-id="5f941-117">La valeur doit être supérieure ou égale à 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="5f941-117">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="5f941-118">*Côtés* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f941-118">*Sides* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f941-119">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f941-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5f941-120">Nombre de côtés dans une section croisée.</span><span class="sxs-lookup"><span data-stu-id="5f941-120">Number of sides in a cross-section.</span></span> <span data-ttu-id="5f941-121">La valeur doit être supérieure ou égale à 3.</span><span class="sxs-lookup"><span data-stu-id="5f941-121">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="5f941-122">*Anneaux* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f941-122">*Rings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f941-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f941-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5f941-124">Nombre d’anneaux composant le tore.</span><span class="sxs-lookup"><span data-stu-id="5f941-124">Number of rings making up the torus.</span></span> <span data-ttu-id="5f941-125">La valeur doit être supérieure ou égale à 3.</span><span class="sxs-lookup"><span data-stu-id="5f941-125">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="5f941-126">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5f941-126">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f941-127">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="5f941-127">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="5f941-128">Adresse d’un pointeur vers la forme de sortie, une interface [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="5f941-128">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="5f941-129">*ppAdjacency* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5f941-129">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f941-130">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5f941-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="5f941-131">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="5f941-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="5f941-132">Quand la méthode est retournée, ce paramètre est rempli avec un tableau de trois DWORDs par visage qui spécifient les trois voisins pour chaque visage de la maille.</span><span class="sxs-lookup"><span data-stu-id="5f941-132">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="5f941-133">La **valeur null** peut être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5f941-133">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f941-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f941-134">Return value</span></span>

<span data-ttu-id="5f941-135">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5f941-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5f941-136">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5f941-136">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5f941-137">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5f941-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f941-138">Notes</span><span class="sxs-lookup"><span data-stu-id="5f941-138">Remarks</span></span>

<span data-ttu-id="5f941-139">Le tore créé est centré au niveau de l’origine et son axe est aligné avec l’axe z.</span><span class="sxs-lookup"><span data-stu-id="5f941-139">The created torus is centered at the origin, and its axis is aligned with the z-axis.</span></span> <span data-ttu-id="5f941-140">Le rayon interne du tore est le rayon de la coupe croisée (rayon mineur), et le rayon externe du tore est le rayon du trou central.</span><span class="sxs-lookup"><span data-stu-id="5f941-140">The inner radius of the torus is the radius of the cross-section (the minor radius), and the outer radius of the torus is the radius of the central hole.</span></span>

<span data-ttu-id="5f941-141">Cette fonction retourne un maillage qui peut être utilisé ultérieurement pour le dessin ou la manipulation par l’application.</span><span class="sxs-lookup"><span data-stu-id="5f941-141">This function returns a mesh that can be used later for drawing or manipulation by the application.</span></span>

<span data-ttu-id="5f941-142">Cette fonction crée une maille avec l' \_ option de création managée D3DXMESH et [D3DFVF \_ xyz \| D3DFVF \_ ](d3dfvf.md) le format de vertex flexible normal.</span><span class="sxs-lookup"><span data-stu-id="5f941-142">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f941-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f941-143">Requirements</span></span>



| <span data-ttu-id="5f941-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f941-144">Requirement</span></span> | <span data-ttu-id="5f941-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f941-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f941-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f941-146">Header</span></span><br/>  | <dl> <span data-ttu-id="5f941-147"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f941-147"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="5f941-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5f941-148">Library</span></span><br/> | <dl> <span data-ttu-id="5f941-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f941-149"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5f941-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f941-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f941-151">Fonctions de dessin de forme</span><span class="sxs-lookup"><span data-stu-id="5f941-151">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
