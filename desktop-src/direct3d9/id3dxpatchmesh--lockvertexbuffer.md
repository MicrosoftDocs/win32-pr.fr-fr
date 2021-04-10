---
description: Verrouille la mémoire tampon de vertex.
ms.assetid: f7e4f27d-1b40-4b0d-8173-48a0b15cfc95
title: 'ID3DXPatchMesh :: LockVertexBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d88d8a1da7ae544c5647fc844cda4966cfee7b10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870150"
---
# <a name="id3dxpatchmeshlockvertexbuffer-method"></a><span data-ttu-id="585db-103">ID3DXPatchMesh :: LockVertexBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="585db-103">ID3DXPatchMesh::LockVertexBuffer method</span></span>

<span data-ttu-id="585db-104">Verrouille la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="585db-104">Lock the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="585db-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="585db-105">Syntax</span></span>


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="585db-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="585db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="585db-107">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="585db-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="585db-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="585db-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="585db-109">Combinaison de zéro ou plusieurs indicateurs de verrouillage qui décrivent le type de verrou à effectuer.</span><span class="sxs-lookup"><span data-stu-id="585db-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="585db-110">Pour cette méthode, les indicateurs valides sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="585db-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="585db-111">D3DLOCK \_ Ignorer</span><span class="sxs-lookup"><span data-stu-id="585db-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="585db-112">D3DLOCK \_ aucune \_ \_ mise à jour incorrecte</span><span class="sxs-lookup"><span data-stu-id="585db-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="585db-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="585db-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="585db-114">D3DLOCK en \_ lecture seule</span><span class="sxs-lookup"><span data-stu-id="585db-114">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="585db-115">D3DLOCK \_ NOOVERWRITE</span><span class="sxs-lookup"><span data-stu-id="585db-115">D3DLOCK\_NOOVERWRITE</span></span>

<span data-ttu-id="585db-116">Pour obtenir une description des indicateurs, consultez [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="585db-116">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="585db-117">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="585db-117">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="585db-118">Type : **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="585db-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="585db-119">\*Pointeur void vers une mémoire tampon contenant les données de vertex retournées.</span><span class="sxs-lookup"><span data-stu-id="585db-119">VOID\* pointer to a memory buffer containing the returned vertex data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="585db-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="585db-120">Return value</span></span>

<span data-ttu-id="585db-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="585db-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="585db-122">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="585db-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="585db-123">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="585db-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="585db-124">Notes</span><span class="sxs-lookup"><span data-stu-id="585db-124">Remarks</span></span>

<span data-ttu-id="585db-125">La mémoire tampon de vertex est généralement verrouillée, écrite dans, puis déverrouillée pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="585db-125">The vertex buffer is usually locked, written to, and then unlocked for reading.</span></span>

<span data-ttu-id="585db-126">Les maillages de correctifs utilisent des mémoires tampons d’index 16 bits.</span><span class="sxs-lookup"><span data-stu-id="585db-126">Patch meshes use 16-bit index buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="585db-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="585db-127">Requirements</span></span>



| <span data-ttu-id="585db-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="585db-128">Requirement</span></span> | <span data-ttu-id="585db-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="585db-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="585db-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="585db-130">Header</span></span><br/>  | <dl> <span data-ttu-id="585db-131"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="585db-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="585db-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="585db-132">Library</span></span><br/> | <dl> <span data-ttu-id="585db-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="585db-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="585db-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="585db-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="585db-135">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="585db-135">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
