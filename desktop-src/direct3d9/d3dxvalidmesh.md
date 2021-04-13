---
description: Valide une maille.
ms.assetid: e5bec2f3-e914-4677-8114-77c71b8a586e
title: D3DXValidMesh, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 469b9b32072107885417266266f804a955301668
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322821"
---
# <a name="d3dxvalidmesh-function"></a><span data-ttu-id="aaa4a-103">D3DXValidMesh fonction)</span><span class="sxs-lookup"><span data-stu-id="aaa4a-103">D3DXValidMesh function</span></span>

<span data-ttu-id="aaa4a-104">Valide une maille.</span><span class="sxs-lookup"><span data-stu-id="aaa4a-104">Validates a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaa4a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aaa4a-105">Syntax</span></span>


```C++
HRESULT D3DXValidMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacency,
  _Out_       LPD3DXBUFFER *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="aaa4a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aaa4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaa4a-107">*pMeshIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aaa4a-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa4a-108">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="aaa4a-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="aaa4a-109">Pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage à tester.</span><span class="sxs-lookup"><span data-stu-id="aaa4a-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="aaa4a-110">*pAdjacency* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aaa4a-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa4a-111">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="aaa4a-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="aaa4a-112">Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque face de la maille à tester.</span><span class="sxs-lookup"><span data-stu-id="aaa4a-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="aaa4a-113">*ppErrorsAndWarnings* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="aaa4a-113">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aaa4a-114">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="aaa4a-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="aaa4a-115">Retourne une mémoire tampon contenant une chaîne d’erreurs et d’avertissements, qui expliquent les problèmes détectés dans la maille.</span><span class="sxs-lookup"><span data-stu-id="aaa4a-115">Returns a buffer containing a string of errors and warnings, which explain the problems found in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaa4a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aaa4a-116">Return value</span></span>

<span data-ttu-id="aaa4a-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aaa4a-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aaa4a-118">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="aaa4a-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="aaa4a-119">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DXERR \_ INVALIDMESH, D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="aaa4a-119">If the function fails, the return value can be one of the following: D3DXERR\_INVALIDMESH, D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaa4a-120">Notes</span><span class="sxs-lookup"><span data-stu-id="aaa4a-120">Remarks</span></span>

<span data-ttu-id="aaa4a-121">Cette méthode valide le maillage en vérifiant les index non valides.</span><span class="sxs-lookup"><span data-stu-id="aaa4a-121">This method validates the mesh by checking for invalid indices.</span></span> <span data-ttu-id="aaa4a-122">Les informations d’erreur sont disponibles à partir de la sortie du débogueur.</span><span class="sxs-lookup"><span data-stu-id="aaa4a-122">Error information is available from the debugger output.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaa4a-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aaa4a-123">Requirements</span></span>



| <span data-ttu-id="aaa4a-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aaa4a-124">Requirement</span></span> | <span data-ttu-id="aaa4a-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="aaa4a-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaa4a-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="aaa4a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="aaa4a-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaa4a-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="aaa4a-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aaa4a-128">Library</span></span><br/> | <dl> <span data-ttu-id="aaa4a-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aaa4a-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aaa4a-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aaa4a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaa4a-131">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="aaa4a-131">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
