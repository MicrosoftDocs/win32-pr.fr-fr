---
description: Convertit les données représentatives de point en informations d’adjacence de maillage.
ms.assetid: 6ae40486-74be-45a8-9971-f20517c8dcf0
title: 'ID3DXBaseMesh :: ConvertPointRepsToAdjacency, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertPointRepsToAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b1c38d7790d575bdf6794e0e21f1c4043e80257c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539440"
---
# <a name="id3dxbasemeshconvertpointrepstoadjacency-method"></a><span data-ttu-id="1e83a-103">ID3DXBaseMesh :: ConvertPointRepsToAdjacency, méthode</span><span class="sxs-lookup"><span data-stu-id="1e83a-103">ID3DXBaseMesh::ConvertPointRepsToAdjacency method</span></span>

<span data-ttu-id="1e83a-104">Convertit les données représentatives de point en informations d’adjacence de maillage.</span><span class="sxs-lookup"><span data-stu-id="1e83a-104">Converts point representative data to mesh adjacency information.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e83a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e83a-105">Syntax</span></span>


```C++
HRESULT ConvertPointRepsToAdjacency(
  [in]      const DWORD *pPRep,
  [in, out]       DWORD *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="1e83a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e83a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e83a-107">*pPRep* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e83a-107">*pPRep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e83a-108">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1e83a-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1e83a-109">Pointeur vers un tableau d’une valeur DWORD par vertex de la maille qui contient les données représentatives du point.</span><span class="sxs-lookup"><span data-stu-id="1e83a-109">Pointer to an array of one DWORD per vertex of the mesh that contains point representative data.</span></span> <span data-ttu-id="1e83a-110">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1e83a-110">This parameter is optional.</span></span> <span data-ttu-id="1e83a-111">Si vous fournissez une valeur **null** , ce paramètre est interprété comme un tableau « Identity ».</span><span class="sxs-lookup"><span data-stu-id="1e83a-111">Supplying a **NULL** value will cause this parameter to be interpreted as an "identity" array.</span></span>

</dd> <dt>

<span data-ttu-id="1e83a-112">*pAdjacency* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1e83a-112">*pAdjacency* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e83a-113">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1e83a-113">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1e83a-114">Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque face de la maille.</span><span class="sxs-lookup"><span data-stu-id="1e83a-114">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="1e83a-115">Le nombre d’octets dans ce tableau doit être au moins égal à 3 \* [**ID3DXBaseMesh :: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="1e83a-115">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e83a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e83a-116">Return value</span></span>

<span data-ttu-id="1e83a-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1e83a-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1e83a-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1e83a-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1e83a-119">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1e83a-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e83a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e83a-120">Requirements</span></span>



| <span data-ttu-id="1e83a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e83a-121">Requirement</span></span> | <span data-ttu-id="1e83a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e83a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e83a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e83a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1e83a-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e83a-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1e83a-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1e83a-125">Library</span></span><br/> | <dl> <span data-ttu-id="1e83a-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e83a-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1e83a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e83a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e83a-128">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="1e83a-128">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
