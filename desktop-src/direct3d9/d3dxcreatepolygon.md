---
description: Utilise un système de coordonnées droitier pour créer un maillage contenant un polygone à deux côtés.
ms.assetid: f3313f55-3e60-4440-8bea-d2886b636c9a
title: D3DXCreatePolygon, fonction (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePolygon
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94a7e48f512d25ca53d1f3ff80889a013e2ecdcb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043106"
---
# <a name="d3dxcreatepolygon-function"></a><span data-ttu-id="ab787-103">D3DXCreatePolygon fonction)</span><span class="sxs-lookup"><span data-stu-id="ab787-103">D3DXCreatePolygon function</span></span>

<span data-ttu-id="ab787-104">Utilise un système de coordonnées droitier pour créer un maillage contenant un polygone à deux côtés.</span><span class="sxs-lookup"><span data-stu-id="ab787-104">Uses a left-handed coordinate system to create a mesh containing an n-sided polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab787-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab787-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePolygon(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Length,
  _In_  UINT              Sides,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="ab787-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab787-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab787-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab787-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab787-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ab787-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ab787-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) représentant l’appareil associé au maillage de polygone créé.</span><span class="sxs-lookup"><span data-stu-id="ab787-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created polygon mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ab787-110">*Longueur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab787-110">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab787-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab787-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab787-112">Longueur de chaque côté.</span><span class="sxs-lookup"><span data-stu-id="ab787-112">Length of each side.</span></span>

</dd> <dt>

<span data-ttu-id="ab787-113">*Côtés* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab787-113">*Sides* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab787-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab787-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab787-115">Nombre de côtés pour le polygone.</span><span class="sxs-lookup"><span data-stu-id="ab787-115">Number of sides for the polygon.</span></span> <span data-ttu-id="ab787-116">La valeur doit être supérieure ou égale à 3.</span><span class="sxs-lookup"><span data-stu-id="ab787-116">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="ab787-117">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ab787-117">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab787-118">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab787-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="ab787-119">Adresse d’un pointeur vers la forme de sortie, une interface [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="ab787-119">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="ab787-120">*ppAdjacency* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ab787-120">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab787-121">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab787-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ab787-122">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ab787-122">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="ab787-123">Quand la méthode est retournée, ce paramètre est rempli avec un tableau de trois DWORDs par visage qui spécifient les trois voisins pour chaque visage de la maille.</span><span class="sxs-lookup"><span data-stu-id="ab787-123">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="ab787-124">La **valeur null** peut être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ab787-124">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab787-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ab787-125">Return value</span></span>

<span data-ttu-id="ab787-126">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab787-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab787-127">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ab787-127">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ab787-128">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ab787-128">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab787-129">Notes</span><span class="sxs-lookup"><span data-stu-id="ab787-129">Remarks</span></span>

<span data-ttu-id="ab787-130">Le polygone créé est centré à l’origine.</span><span class="sxs-lookup"><span data-stu-id="ab787-130">The created polygon is centered at the origin.</span></span>

<span data-ttu-id="ab787-131">Cette fonction crée une maille avec l' \_ option de création managée D3DXMESH et [D3DFVF \_ xyz \| D3DFVF \_ ](d3dfvf.md) le format de vertex flexible normal.</span><span class="sxs-lookup"><span data-stu-id="ab787-131">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab787-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab787-132">Requirements</span></span>



| <span data-ttu-id="ab787-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab787-133">Requirement</span></span> | <span data-ttu-id="ab787-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab787-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab787-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab787-135">Header</span></span><br/>  | <dl> <span data-ttu-id="ab787-136"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab787-136"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="ab787-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ab787-137">Library</span></span><br/> | <dl> <span data-ttu-id="ab787-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab787-138"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ab787-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab787-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab787-140">Fonctions de dessin de forme</span><span class="sxs-lookup"><span data-stu-id="ab787-140">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
