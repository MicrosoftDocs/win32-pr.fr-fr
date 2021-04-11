---
description: Convertit les informations d’adjacence de maillage en un tableau de représentants de point.
ms.assetid: b8914f9c-8550-498d-813d-bb1afe0fb5b2
title: 'ID3DXBaseMesh :: ConvertAdjacencyToPointReps, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertAdjacencyToPointReps
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3a4827473cce115f742a85b99732d09a2c5efa4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211737"
---
# <a name="id3dxbasemeshconvertadjacencytopointreps-method"></a><span data-ttu-id="e234f-103">ID3DXBaseMesh :: ConvertAdjacencyToPointReps, méthode</span><span class="sxs-lookup"><span data-stu-id="e234f-103">ID3DXBaseMesh::ConvertAdjacencyToPointReps method</span></span>

<span data-ttu-id="e234f-104">Convertit les informations d’adjacence de maillage en un tableau de représentants de point.</span><span class="sxs-lookup"><span data-stu-id="e234f-104">Converts mesh adjacency information to an array of point representatives.</span></span>

## <a name="syntax"></a><span data-ttu-id="e234f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e234f-105">Syntax</span></span>


```C++
HRESULT ConvertAdjacencyToPointReps(
  [in]      const DWORD *pAdjacency,
  [in, out]       DWORD *pPRep
);
```



## <a name="parameters"></a><span data-ttu-id="e234f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e234f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e234f-107">*pAdjacency* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e234f-107">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e234f-108">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e234f-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e234f-109">Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque face de la maille.</span><span class="sxs-lookup"><span data-stu-id="e234f-109">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="e234f-110">Le nombre d’octets dans ce tableau doit être au moins égal à 3 \* [**ID3DXBaseMesh :: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="e234f-110">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> <dt>

<span data-ttu-id="e234f-111">*pPRep* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e234f-111">*pPRep* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e234f-112">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e234f-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e234f-113">Pointeur vers un tableau d’une valeur DWORD par vertex de la maille qui sera remplie avec des données représentatives de point.</span><span class="sxs-lookup"><span data-stu-id="e234f-113">Pointer to an array of one DWORD per vertex of the mesh that will be filled with point representative data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e234f-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e234f-114">Return value</span></span>

<span data-ttu-id="e234f-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e234f-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e234f-116">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e234f-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e234f-117">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e234f-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e234f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e234f-118">Requirements</span></span>



| <span data-ttu-id="e234f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e234f-119">Requirement</span></span> | <span data-ttu-id="e234f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e234f-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e234f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e234f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e234f-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e234f-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e234f-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e234f-123">Library</span></span><br/> | <dl> <span data-ttu-id="e234f-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e234f-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e234f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e234f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e234f-126">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="e234f-126">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
