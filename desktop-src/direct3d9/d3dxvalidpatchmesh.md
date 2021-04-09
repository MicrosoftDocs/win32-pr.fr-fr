---
description: Valide un maillage de correctifs, en retournant le nombre de Dégénérations de vertex et de correctifs.
ms.assetid: a95ff9d9-d476-42ac-8d7e-1dc42418f763
title: D3DXValidPatchMesh, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87d7fbe15c78a8b768d845e6a23cc084b69f3e02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953831"
---
# <a name="d3dxvalidpatchmesh-function"></a><span data-ttu-id="3f89e-103">D3DXValidPatchMesh fonction)</span><span class="sxs-lookup"><span data-stu-id="3f89e-103">D3DXValidPatchMesh function</span></span>

<span data-ttu-id="3f89e-104">Valide un maillage de correctifs, en retournant le nombre de Dégénérations de vertex et de correctifs.</span><span class="sxs-lookup"><span data-stu-id="3f89e-104">Validates a patch mesh, returning the number of degenerate vertices and patches.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f89e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f89e-105">Syntax</span></span>


```C++
HRESULT D3DXValidPatchMesh(
  _In_  LPD3DXPATCHMESH pMeshIn,
  _Out_ DWORD           *pNumDegenerateVertices,
  _Out_ DWORD           *pNumDegeneratePatches,
  _Out_ LPD3DXBUFFER    *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="3f89e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f89e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f89e-107">*pMeshIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3f89e-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f89e-108">Type : **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="3f89e-108">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)**</span></span>

<span data-ttu-id="3f89e-109">Pointeur vers une interface [**ID3DXPatchMesh**](id3dxpatchmesh.md) représentant la maille de correctif à tester.</span><span class="sxs-lookup"><span data-stu-id="3f89e-109">Pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface, representing the patch mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="3f89e-110">*pNumDegenerateVertices* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3f89e-110">*pNumDegenerateVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f89e-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f89e-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3f89e-112">Retourne le nombre de vertex dégénérés dans la maille de correctifs.</span><span class="sxs-lookup"><span data-stu-id="3f89e-112">Returns the number of degenerate vertices in the patch mesh.</span></span>

</dd> <dt>

<span data-ttu-id="3f89e-113">*pNumDegeneratePatches* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3f89e-113">*pNumDegeneratePatches* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f89e-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f89e-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3f89e-115">Retourne le nombre de correctifs dégénérées dans le maillage des correctifs.</span><span class="sxs-lookup"><span data-stu-id="3f89e-115">Returns the number of degenerate patches in the patch mesh.</span></span>

</dd> <dt>

<span data-ttu-id="3f89e-116">*ppErrorsAndWarnings* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3f89e-116">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f89e-117">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f89e-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3f89e-118">Retourne un pointeur vers une mémoire tampon contenant une chaîne d’erreurs et d’avertissements qui expliquent les problèmes détectés dans la maille de correctifs.</span><span class="sxs-lookup"><span data-stu-id="3f89e-118">Returns a pointer to a buffer containing a string of errors and warnings that explain the problems found in the patch mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f89e-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3f89e-119">Return value</span></span>

<span data-ttu-id="3f89e-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3f89e-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3f89e-121">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3f89e-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3f89e-122">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3f89e-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f89e-123">Notes</span><span class="sxs-lookup"><span data-stu-id="3f89e-123">Remarks</span></span>

<span data-ttu-id="3f89e-124">Cette méthode valide le maillage en vérifiant les index non valides.</span><span class="sxs-lookup"><span data-stu-id="3f89e-124">This method validates the mesh by checking for invalid indices.</span></span> <span data-ttu-id="3f89e-125">Les informations d’erreur sont disponibles à partir de la sortie du débogueur.</span><span class="sxs-lookup"><span data-stu-id="3f89e-125">Error information is available from the debugger output.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f89e-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f89e-126">Requirements</span></span>



| <span data-ttu-id="3f89e-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f89e-127">Requirement</span></span> | <span data-ttu-id="3f89e-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f89e-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f89e-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f89e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3f89e-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f89e-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3f89e-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3f89e-131">Library</span></span><br/> | <dl> <span data-ttu-id="3f89e-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f89e-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3f89e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f89e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f89e-134">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="3f89e-134">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
