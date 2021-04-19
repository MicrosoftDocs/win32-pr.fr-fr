---
description: Nettoie un maillage, en le préparant à des fins de simplification.
ms.assetid: 2b586ecc-db87-4b20-a4fc-c8b547bebf65
title: D3DXCleanMesh, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCleanMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5565978dc1ad0e80c33718275ea65080930ce7cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522365"
---
# <a name="d3dxcleanmesh-function"></a><span data-ttu-id="52ee8-103">D3DXCleanMesh fonction)</span><span class="sxs-lookup"><span data-stu-id="52ee8-103">D3DXCleanMesh function</span></span>

<span data-ttu-id="52ee8-104">Nettoie un maillage, en le préparant à des fins de simplification.</span><span class="sxs-lookup"><span data-stu-id="52ee8-104">Cleans a mesh, preparing it for simplification.</span></span>

## <a name="syntax"></a><span data-ttu-id="52ee8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52ee8-105">Syntax</span></span>


```C++
HRESULT D3DXCleanMesh(
  _In_        D3DXCLEANTYPE CleanType,
  _In_        LPD3DXMESH    pMeshIn,
  _In_  const DWORD         *pAdjacencyIn,
  _Out_       LPD3DXMESH    *ppMeshOut,
  _Out_       DWORD         *pAdjacencyOut,
  _Out_       LPD3DXBUFFER  *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="52ee8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52ee8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52ee8-107">*CleanType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52ee8-107">*CleanType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52ee8-108">Type : **[ **D3DXCLEANTYPE**](./d3dxcleantype.md)**</span><span class="sxs-lookup"><span data-stu-id="52ee8-108">Type: **[**D3DXCLEANTYPE**](./d3dxcleantype.md)**</span></span>

<span data-ttu-id="52ee8-109">Opérations de vertex à effectuer en préparation du nettoyage de maillage.</span><span class="sxs-lookup"><span data-stu-id="52ee8-109">Vertex operations to perform in preparation for mesh cleaning.</span></span> <span data-ttu-id="52ee8-110">Consultez [**D3DXCLEANTYPE**](./d3dxcleantype.md).</span><span class="sxs-lookup"><span data-stu-id="52ee8-110">See [**D3DXCLEANTYPE**](./d3dxcleantype.md).</span></span>

</dd> <dt>

<span data-ttu-id="52ee8-111">*pMeshIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52ee8-111">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52ee8-112">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="52ee8-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="52ee8-113">Pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage à nettoyer.</span><span class="sxs-lookup"><span data-stu-id="52ee8-113">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to be cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="52ee8-114">*pAdjacencyIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52ee8-114">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52ee8-115">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="52ee8-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="52ee8-116">Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque face de la maille à nettoyer.</span><span class="sxs-lookup"><span data-stu-id="52ee8-116">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="52ee8-117">*ppMeshOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="52ee8-117">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52ee8-118">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="52ee8-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="52ee8-119">Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage nettoyé retourné.</span><span class="sxs-lookup"><span data-stu-id="52ee8-119">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned cleaned mesh.</span></span> <span data-ttu-id="52ee8-120">Le même maillage est retourné qui a été transmis si aucun nettoyage n’était nécessaire.</span><span class="sxs-lookup"><span data-stu-id="52ee8-120">The same mesh is returned that was passed in if no cleaning was necessary.</span></span>

</dd> <dt>

<span data-ttu-id="52ee8-121">*pAdjacencyOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="52ee8-121">*pAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52ee8-122">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="52ee8-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="52ee8-123">Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage dans le maillage de sortie.</span><span class="sxs-lookup"><span data-stu-id="52ee8-123">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="52ee8-124">*ppErrorsAndWarnings* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="52ee8-124">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52ee8-125">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="52ee8-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="52ee8-126">Retourne une mémoire tampon contenant une chaîne d’erreurs et d’avertissements, qui expliquent les problèmes détectés dans la maille.</span><span class="sxs-lookup"><span data-stu-id="52ee8-126">Returns a buffer containing a string of errors and warnings, which explain the problems found in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52ee8-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="52ee8-127">Return value</span></span>

<span data-ttu-id="52ee8-128">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="52ee8-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="52ee8-129">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="52ee8-129">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="52ee8-130">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="52ee8-130">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="52ee8-131">Notes</span><span class="sxs-lookup"><span data-stu-id="52ee8-131">Remarks</span></span>

<span data-ttu-id="52ee8-132">Cette fonction nettoie un maillage à l’aide de la méthode de nettoyage et des options spécifiées dans le paramètre CleanType.</span><span class="sxs-lookup"><span data-stu-id="52ee8-132">This function cleans a mesh using the cleaning method and options specified in the CleanType parameter.</span></span> <span data-ttu-id="52ee8-133">Pour obtenir une description des options disponibles, consultez l’énumération [**D3DXCLEANTYPE**](./d3dxcleantype.md) .</span><span class="sxs-lookup"><span data-stu-id="52ee8-133">See the [**D3DXCLEANTYPE**](./d3dxcleantype.md) enumeration for a description of the available options.</span></span>

## <a name="requirements"></a><span data-ttu-id="52ee8-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52ee8-134">Requirements</span></span>



| <span data-ttu-id="52ee8-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52ee8-135">Requirement</span></span> | <span data-ttu-id="52ee8-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="52ee8-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52ee8-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="52ee8-137">Header</span></span><br/>  | <dl> <span data-ttu-id="52ee8-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="52ee8-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="52ee8-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="52ee8-139">Library</span></span><br/> | <dl> <span data-ttu-id="52ee8-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52ee8-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="52ee8-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52ee8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52ee8-142">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="52ee8-142">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
