---
description: Utilise un système de coordonnées droitier pour créer un maillage contenant un théière.
ms.assetid: c002d6d4-1829-4293-9a86-d8560d6ec0e9
title: D3DXCreateTeapot, fonction (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTeapot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 13f5ed44bdc31958729209f01183eba409298fcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211771"
---
# <a name="d3dxcreateteapot-function"></a><span data-ttu-id="3ca21-103">D3DXCreateTeapot fonction)</span><span class="sxs-lookup"><span data-stu-id="3ca21-103">D3DXCreateTeapot function</span></span>

<span data-ttu-id="3ca21-104">Utilise un système de coordonnées droitier pour créer un maillage contenant un théière.</span><span class="sxs-lookup"><span data-stu-id="3ca21-104">Uses a left-handed coordinate system to create a mesh containing a teapot.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ca21-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ca21-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTeapot(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="3ca21-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ca21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ca21-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3ca21-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca21-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="3ca21-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="3ca21-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la maille théière créée.</span><span class="sxs-lookup"><span data-stu-id="3ca21-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created teapot mesh.</span></span>

</dd> <dt>

<span data-ttu-id="3ca21-110">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3ca21-110">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca21-111">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="3ca21-111">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="3ca21-112">Adresse d’un pointeur vers la forme de sortie, une interface [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="3ca21-112">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="3ca21-113">*ppAdjacency* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3ca21-113">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca21-114">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3ca21-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3ca21-115">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="3ca21-115">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="3ca21-116">Quand la méthode est retournée, ce paramètre est rempli avec un tableau de trois DWORDs par visage qui spécifient les trois voisins pour chaque visage de la maille.</span><span class="sxs-lookup"><span data-stu-id="3ca21-116">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="3ca21-117">La **valeur null** peut être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3ca21-117">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ca21-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3ca21-118">Return value</span></span>

<span data-ttu-id="3ca21-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3ca21-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3ca21-120">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3ca21-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3ca21-121">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3ca21-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ca21-122">Notes</span><span class="sxs-lookup"><span data-stu-id="3ca21-122">Remarks</span></span>

<span data-ttu-id="3ca21-123">Cette fonction crée une maille avec l' \_ option de création managée D3DXMESH et [D3DFVF \_ xyz \| D3DFVF \_ ](d3dfvf.md) le format de vertex flexible normal.</span><span class="sxs-lookup"><span data-stu-id="3ca21-123">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ca21-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ca21-124">Requirements</span></span>



| <span data-ttu-id="3ca21-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ca21-125">Requirement</span></span> | <span data-ttu-id="3ca21-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ca21-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca21-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="3ca21-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3ca21-128"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ca21-128"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="3ca21-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3ca21-129">Library</span></span><br/> | <dl> <span data-ttu-id="3ca21-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ca21-130"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3ca21-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ca21-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ca21-132">Fonctions de dessin de forme</span><span class="sxs-lookup"><span data-stu-id="3ca21-132">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
