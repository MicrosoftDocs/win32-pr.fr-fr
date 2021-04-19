---
description: Verrouille la mémoire tampon d’attribut.
ms.assetid: 6e05e613-ca93-41b0-a3b3-a9564ada3b0c
title: 'ID3DXPatchMesh :: LockAttributeBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71e50fdc27f3f50b560324c74f5a1609f900772d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523860"
---
# <a name="id3dxpatchmeshlockattributebuffer-method"></a><span data-ttu-id="cb380-103">ID3DXPatchMesh :: LockAttributeBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="cb380-103">ID3DXPatchMesh::LockAttributeBuffer method</span></span>

<span data-ttu-id="cb380-104">Verrouille la mémoire tampon d’attribut.</span><span class="sxs-lookup"><span data-stu-id="cb380-104">Locks the attribute buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb380-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb380-105">Syntax</span></span>


```C++
HRESULT LockAttributeBuffer(
  [in]          DWORD flags,
  [out, retval] DWORD **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="cb380-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb380-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb380-107">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cb380-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb380-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb380-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cb380-109">Combinaison de zéro ou plusieurs indicateurs de verrouillage qui décrivent le type de verrou à effectuer.</span><span class="sxs-lookup"><span data-stu-id="cb380-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="cb380-110">Pour cette méthode, les indicateurs valides sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="cb380-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="cb380-111">D3DLOCK \_ Ignorer</span><span class="sxs-lookup"><span data-stu-id="cb380-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="cb380-112">D3DLOCK \_ aucune \_ \_ mise à jour incorrecte</span><span class="sxs-lookup"><span data-stu-id="cb380-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="cb380-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="cb380-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="cb380-114">D3DLOCK en \_ lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb380-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="cb380-115">Pour obtenir une description des indicateurs, consultez [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="cb380-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb380-116">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cb380-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cb380-117">Type : **[ **DWORD**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cb380-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="cb380-118">Adresse d’un pointeur vers une mémoire tampon contenant un DWORD pour chaque face de la maille.</span><span class="sxs-lookup"><span data-stu-id="cb380-118">Address of a pointer to a buffer containing a DWORD for each face in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb380-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb380-119">Return value</span></span>

<span data-ttu-id="cb380-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cb380-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cb380-121">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cb380-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cb380-122">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cb380-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb380-123">Notes</span><span class="sxs-lookup"><span data-stu-id="cb380-123">Remarks</span></span>

<span data-ttu-id="cb380-124">La mémoire tampon d’attribut est généralement verrouillée, écrite dans, puis déverrouillée pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="cb380-124">The attribute buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb380-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb380-125">Requirements</span></span>



| <span data-ttu-id="cb380-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb380-126">Requirement</span></span> | <span data-ttu-id="cb380-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb380-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb380-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb380-128">Header</span></span><br/>  | <dl> <span data-ttu-id="cb380-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb380-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cb380-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cb380-130">Library</span></span><br/> | <dl> <span data-ttu-id="cb380-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb380-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cb380-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb380-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb380-133">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="cb380-133">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
