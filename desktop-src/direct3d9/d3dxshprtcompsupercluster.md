---
description: Utilisé avec les résultats compressés de la version vertex du simulateur de transfert luminance (PRT) précalculé.
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: D3DXSHPRTCompSuperCluster, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSuperCluster
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1daf25dddfaf738ecc2fed9605429a19170177ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322861"
---
# <a name="d3dxshprtcompsupercluster-function"></a><span data-ttu-id="1a5f6-103">D3DXSHPRTCompSuperCluster fonction)</span><span class="sxs-lookup"><span data-stu-id="1a5f6-103">D3DXSHPRTCompSuperCluster function</span></span>

<span data-ttu-id="1a5f6-104">Utilisé avec les résultats compressés de la version vertex du simulateur de transfert luminance (PRT) précalculé.</span><span class="sxs-lookup"><span data-stu-id="1a5f6-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="1a5f6-105">Génère des « superclusters », qui sont des groupes de clusters qui peuvent être dessinés dans le même appel de dessin.</span><span class="sxs-lookup"><span data-stu-id="1a5f6-105">Generates "superclusters," which are groups of clusters that can be drawn in the same draw call.</span></span> <span data-ttu-id="1a5f6-106">Un algorithme gourmand qui minimise le surdessin est utilisé pour regrouper les clusters.</span><span class="sxs-lookup"><span data-stu-id="1a5f6-106">A greedy algorithm that minimizes overdraw is used to group the clusters.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a5f6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a5f6-107">Syntax</span></span>


```C++
HRESULT D3DXSHPRTCompSuperCluster(
  _In_    UINT       *pClusterIDs,
  _In_    LPD3DXMESH pScene,
  _In_    UINT       MaxNumClusters,
  _In_    UINT       NumClusters,
  _Inout_ UINT       *pSClusterIDs,
  _Inout_ UINT       *pNumSCs
);
```



## <a name="parameters"></a><span data-ttu-id="1a5f6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a5f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a5f6-109">*pClusterIDs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a5f6-109">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5f6-110">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a5f6-110">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1a5f6-111">Pointeur vers un ID de cluster NumVerts (extrait d’une mémoire tampon compressée.)</span><span class="sxs-lookup"><span data-stu-id="1a5f6-111">Pointer to a NumVerts cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="1a5f6-112">*pScene* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a5f6-112">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5f6-113">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="1a5f6-113">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="1a5f6-114">Pointeur vers un maillage qui représente la scène composite transmise au simulateur.</span><span class="sxs-lookup"><span data-stu-id="1a5f6-114">Pointer to a mesh that represents composite scene passed to the simulator.</span></span> <span data-ttu-id="1a5f6-115">Consultez [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="1a5f6-115">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a5f6-116">*MaxNumClusters* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a5f6-116">*MaxNumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5f6-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a5f6-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a5f6-118">Nombre maximal de clusters alloués par Super cluster.</span><span class="sxs-lookup"><span data-stu-id="1a5f6-118">Maximum number of clusters allocated per super cluster.</span></span>

</dd> <dt>

<span data-ttu-id="1a5f6-119">*NumClusters* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a5f6-119">*NumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5f6-120">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a5f6-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a5f6-121">Nombre de clusters calculés dans le simulateur.</span><span class="sxs-lookup"><span data-stu-id="1a5f6-121">Number of clusters computed in the simulator.</span></span>

</dd> <dt>

<span data-ttu-id="1a5f6-122">*pSClusterIDs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1a5f6-122">*pSClusterIDs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5f6-123">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a5f6-123">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1a5f6-124">Pointeur vers un tableau de longueur *NumClusters*.</span><span class="sxs-lookup"><span data-stu-id="1a5f6-124">Pointer to an array of length *NumClusters*.</span></span> <span data-ttu-id="1a5f6-125">Contient l’index du Super cluster auquel le cluster correspondant a été affecté.</span><span class="sxs-lookup"><span data-stu-id="1a5f6-125">Contains the index of the super cluster to which the corresponding cluster was assigned.</span></span>

</dd> <dt>

<span data-ttu-id="1a5f6-126">*pNumSCs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1a5f6-126">*pNumSCs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5f6-127">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a5f6-127">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1a5f6-128">Nombre de Super clusters alloués.</span><span class="sxs-lookup"><span data-stu-id="1a5f6-128">Number of super clusters allocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a5f6-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a5f6-129">Return value</span></span>

<span data-ttu-id="1a5f6-130">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1a5f6-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1a5f6-131">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1a5f6-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1a5f6-132">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1a5f6-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a5f6-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a5f6-133">Requirements</span></span>



| <span data-ttu-id="1a5f6-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a5f6-134">Requirement</span></span> | <span data-ttu-id="1a5f6-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a5f6-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a5f6-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a5f6-136">Header</span></span><br/>  | <dl> <span data-ttu-id="1a5f6-137"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a5f6-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1a5f6-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1a5f6-138">Library</span></span><br/> | <dl> <span data-ttu-id="1a5f6-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a5f6-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1a5f6-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a5f6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a5f6-141">Fonctions de transfert luminance précalculées</span><span class="sxs-lookup"><span data-stu-id="1a5f6-141">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
