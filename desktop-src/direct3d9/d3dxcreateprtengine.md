---
description: Crée un objet ID3DXPRTEngine capable de générer efficacement des simulations de transfert de luminance précalculées (PRT) d’une scène 3D.
ms.assetid: fdfe02b5-03fb-4bee-a53b-012ae3572644
title: D3DXCreatePRTEngine, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTEngine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b76b58953de81041922659c3315bba9cdf7788b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530928"
---
# <a name="d3dxcreateprtengine-function"></a><span data-ttu-id="a952c-103">D3DXCreatePRTEngine fonction)</span><span class="sxs-lookup"><span data-stu-id="a952c-103">D3DXCreatePRTEngine function</span></span>

<span data-ttu-id="a952c-104">Crée un objet [**ID3DXPRTEngine**](id3dxprtengine.md) capable de générer efficacement des simulations de transfert de luminance précalculées (PRT) d’une scène 3D.</span><span class="sxs-lookup"><span data-stu-id="a952c-104">Creates an [**ID3DXPRTEngine**](id3dxprtengine.md) object that can efficiently generate precomputed radiance transfer (PRT) simulations of a 3D scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="a952c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a952c-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTEngine(
  _In_    LPD3DXMESH      pMesh,
  _In_    DWORD           *pAdjacency,
  _In_    BOOL            ExtractUVs,
  _In_    LPD3DXMESH      pBlockerMesh,
  _Inout_ LPD3DXPRTENGINE ppEngine
);
```



## <a name="parameters"></a><span data-ttu-id="a952c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a952c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a952c-107">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a952c-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a952c-108">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="a952c-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="a952c-109">Pointeur vers un objet de maillage [**ID3DXMesh**](id3dxmesh.md) d’entrée qui modélise la scène 3D.</span><span class="sxs-lookup"><span data-stu-id="a952c-109">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object that models the 3D scene.</span></span> <span data-ttu-id="a952c-110">Ce maillage doit avoir une table d’attributs dans laquelle les vertex sont dans un attribut unique.</span><span class="sxs-lookup"><span data-stu-id="a952c-110">This mesh must have an attribute table in which vertices are in a unique attribute.</span></span>

</dd> <dt>

<span data-ttu-id="a952c-111">*pAdjacency* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a952c-111">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a952c-112">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a952c-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a952c-113">Pointeur facultatif vers un tableau de trois DWORDs par visage à remplir avec des indices de face adjacente.</span><span class="sxs-lookup"><span data-stu-id="a952c-113">Optional pointer to an array of three DWORDs per face to be filled with adjacent face indices.</span></span> <span data-ttu-id="a952c-114">Le nombre d’octets dans ce tableau doit être au moins égal à ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)).</span><span class="sxs-lookup"><span data-stu-id="a952c-114">The number of bytes in this array must be at least ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof(DWORD)).</span></span> <span data-ttu-id="a952c-115">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a952c-115">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a952c-116">*ExtractUVs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a952c-116">*ExtractUVs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a952c-117">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a952c-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a952c-118">Si la **valeur est true**, les textures sont utilisées pour stocker les vecteurs ALBEDOS ou PRT.</span><span class="sxs-lookup"><span data-stu-id="a952c-118">If **TRUE**, textures will be used to store albedos or PRT vectors.</span></span>

</dd> <dt>

<span data-ttu-id="a952c-119">*pBlockerMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a952c-119">*pBlockerMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a952c-120">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="a952c-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="a952c-121">Pointeur vers un objet de maillage [**ID3DXMesh**](id3dxmesh.md) facultatif qui bloque la scène 3D.</span><span class="sxs-lookup"><span data-stu-id="a952c-121">Pointer to an optional [**ID3DXMesh**](id3dxmesh.md) mesh object that blocks the 3D scene.</span></span> <span data-ttu-id="a952c-122">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a952c-122">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a952c-123">*ppEngine* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a952c-123">*ppEngine* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a952c-124">Type : **[ **LPD3DXPRTENGINE**](id3dxprtengine.md)**</span><span class="sxs-lookup"><span data-stu-id="a952c-124">Type: **[**LPD3DXPRTENGINE**](id3dxprtengine.md)**</span></span>

<span data-ttu-id="a952c-125">Pointeur vers un objet [**ID3DXPRTEngine**](id3dxprtengine.md) de sortie.</span><span class="sxs-lookup"><span data-stu-id="a952c-125">Pointer to an output [**ID3DXPRTEngine**](id3dxprtengine.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a952c-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a952c-126">Return value</span></span>

<span data-ttu-id="a952c-127">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a952c-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a952c-128">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a952c-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a952c-129">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a952c-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a952c-130">Notes</span><span class="sxs-lookup"><span data-stu-id="a952c-130">Remarks</span></span>

<span data-ttu-id="a952c-131">Utilisez [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) pour combiner plusieurs mailles en une seule interface de maillage.</span><span class="sxs-lookup"><span data-stu-id="a952c-131">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) to combine multiple meshes into a single mesh interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a952c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a952c-132">Requirements</span></span>



| <span data-ttu-id="a952c-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a952c-133">Requirement</span></span> | <span data-ttu-id="a952c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="a952c-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a952c-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="a952c-135">Header</span></span><br/>  | <dl> <span data-ttu-id="a952c-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a952c-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a952c-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a952c-137">Library</span></span><br/> | <dl> <span data-ttu-id="a952c-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a952c-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a952c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a952c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a952c-140">Fonctions de transfert luminance précalculées</span><span class="sxs-lookup"><span data-stu-id="a952c-140">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
