---
description: Verrouillez le tampon d’index.
ms.assetid: b68aff75-9ba6-4088-b35f-f56d700d1aff
title: 'ID3DXPatchMesh :: LockIndexBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 81dc410262ff21ea972d4c501ac3b5d26a361642
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531083"
---
# <a name="id3dxpatchmeshlockindexbuffer-method"></a><span data-ttu-id="4c765-103">ID3DXPatchMesh :: LockIndexBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="4c765-103">ID3DXPatchMesh::LockIndexBuffer method</span></span>

<span data-ttu-id="4c765-104">Verrouillez le tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="4c765-104">Lock the index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c765-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c765-105">Syntax</span></span>


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="4c765-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c765-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c765-107">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c765-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c765-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c765-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c765-109">Combinaison de zéro ou plusieurs indicateurs de verrouillage qui décrivent le type de verrou à effectuer.</span><span class="sxs-lookup"><span data-stu-id="4c765-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="4c765-110">Pour cette méthode, les indicateurs valides sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="4c765-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="4c765-111">D3DLOCK \_ Ignorer</span><span class="sxs-lookup"><span data-stu-id="4c765-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="4c765-112">D3DLOCK \_ aucune \_ \_ mise à jour incorrecte</span><span class="sxs-lookup"><span data-stu-id="4c765-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="4c765-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="4c765-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="4c765-114">D3DLOCK en \_ lecture seule</span><span class="sxs-lookup"><span data-stu-id="4c765-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="4c765-115">Pour obtenir une description des indicateurs, consultez [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="4c765-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c765-116">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4c765-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4c765-117">Type : **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c765-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4c765-118">\*Pointeur void vers une mémoire tampon contenant les données d’index retournées.</span><span class="sxs-lookup"><span data-stu-id="4c765-118">VOID\* pointer to a memory buffer containing the returned index data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c765-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4c765-119">Return value</span></span>

<span data-ttu-id="4c765-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4c765-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4c765-121">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4c765-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4c765-122">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4c765-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c765-123">Notes</span><span class="sxs-lookup"><span data-stu-id="4c765-123">Remarks</span></span>

<span data-ttu-id="4c765-124">La mémoire tampon d’index est généralement verrouillée, écrite dans, puis déverrouillée pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="4c765-124">The index buffer is usually locked, written to, and then unlocked for reading.</span></span> <span data-ttu-id="4c765-125">Les tampons d’index de maillage de correctifs sont des mémoires tampons de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="4c765-125">Patch mesh index buffers are 16-bit buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c765-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c765-126">Requirements</span></span>



| <span data-ttu-id="4c765-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c765-127">Requirement</span></span> | <span data-ttu-id="4c765-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c765-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c765-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c765-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4c765-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c765-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4c765-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4c765-131">Library</span></span><br/> | <dl> <span data-ttu-id="4c765-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c765-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4c765-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c765-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c765-134">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="4c765-134">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="4c765-135">**D3DXCreatePatchMesh**</span><span class="sxs-lookup"><span data-stu-id="4c765-135">**D3DXCreatePatchMesh**</span></span>](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
