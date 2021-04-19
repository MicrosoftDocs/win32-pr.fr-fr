---
description: Verrouille la mémoire tampon de maillage qui contient les données d’attribut de maillage et retourne un pointeur vers celle-ci.
ms.assetid: 17a321b8-bfb4-4018-869f-6b09e0a811eb
title: 'ID3DXMesh :: LockAttributeBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 901cb98a9d75d08b6412d6fdca841d403064354b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527092"
---
# <a name="id3dxmeshlockattributebuffer-method"></a><span data-ttu-id="47624-103">ID3DXMesh :: LockAttributeBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="47624-103">ID3DXMesh::LockAttributeBuffer method</span></span>

<span data-ttu-id="47624-104">Verrouille la mémoire tampon de maillage qui contient les données d’attribut de maillage et retourne un pointeur vers celle-ci.</span><span class="sxs-lookup"><span data-stu-id="47624-104">Locks the mesh buffer that contains the mesh attribute data, and returns a pointer to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="47624-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47624-105">Syntax</span></span>


```C++
HRESULT LockAttributeBuffer(
  [in]  DWORD Flags,
  [out] DWORD **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="47624-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47624-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47624-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="47624-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47624-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47624-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47624-109">Combinaison de zéro ou plusieurs indicateurs de verrouillage qui décrivent le type de verrou à effectuer.</span><span class="sxs-lookup"><span data-stu-id="47624-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="47624-110">Pour cette méthode, les indicateurs valides sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="47624-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="47624-111">D3DLOCK \_ Ignorer</span><span class="sxs-lookup"><span data-stu-id="47624-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="47624-112">D3DLOCK \_ aucune \_ \_ mise à jour incorrecte</span><span class="sxs-lookup"><span data-stu-id="47624-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="47624-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="47624-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="47624-114">D3DLOCK en \_ lecture seule</span><span class="sxs-lookup"><span data-stu-id="47624-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="47624-115">Pour obtenir une description des indicateurs, consultez [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="47624-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="47624-116">*ppData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="47624-116">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47624-117">Type : **[ **DWORD**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="47624-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="47624-118">Adresse d’un pointeur vers une mémoire tampon contenant un DWORD pour chaque face de la maille.</span><span class="sxs-lookup"><span data-stu-id="47624-118">Address of a pointer to a buffer containing a DWORD for each face in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47624-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47624-119">Return value</span></span>

<span data-ttu-id="47624-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="47624-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="47624-121">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="47624-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="47624-122">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="47624-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="47624-123">Notes</span><span class="sxs-lookup"><span data-stu-id="47624-123">Remarks</span></span>

<span data-ttu-id="47624-124">Si [**ID3DXMesh :: Optimize**](id3dxmesh--optimize.md) a été appelé, la maille aura également une table d’attributs accessible à l’aide de la méthode [**ID3DXBaseMesh :: GetAttributeTable**](id3dxbasemesh--getattributetable.md) .</span><span class="sxs-lookup"><span data-stu-id="47624-124">If [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) has been called, the mesh will also have an attribute table that can be accessed using the [**ID3DXBaseMesh::GetAttributeTable**](id3dxbasemesh--getattributetable.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="47624-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47624-125">Requirements</span></span>



| <span data-ttu-id="47624-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47624-126">Requirement</span></span> | <span data-ttu-id="47624-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="47624-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47624-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="47624-128">Header</span></span><br/>  | <dl> <span data-ttu-id="47624-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="47624-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="47624-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="47624-130">Library</span></span><br/> | <dl> <span data-ttu-id="47624-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47624-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="47624-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47624-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47624-133">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="47624-133">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="47624-134">**ID3DXMesh::UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="47624-134">**ID3DXMesh::UnlockAttributeBuffer**</span></span>](id3dxmesh--unlockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="47624-135">**ID3DXBaseMesh::GetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="47624-135">**ID3DXBaseMesh::GetAttributeTable**</span></span>](id3dxbasemesh--getattributetable.md)
</dt> <dt>

[<span data-ttu-id="47624-136">**ID3DXMesh::SetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="47624-136">**ID3DXMesh::SetAttributeTable**</span></span>](id3dxmesh--setattributetable.md)
</dt> </dl>

 

 
