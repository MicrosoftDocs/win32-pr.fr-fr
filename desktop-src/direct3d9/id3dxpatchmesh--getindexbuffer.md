---
description: Obtient la mémoire tampon d’index de maillage.
ms.assetid: d9152f3b-c8e6-4def-8cf1-a517ca4d34e7
title: 'ID3DXPatchMesh :: GetIndexBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c2730b90f77d33db519d2231a68ab7fdc2b520fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529632"
---
# <a name="id3dxpatchmeshgetindexbuffer-method"></a><span data-ttu-id="99008-103">ID3DXPatchMesh :: GetIndexBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="99008-103">ID3DXPatchMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="99008-104">Obtient la mémoire tampon d’index de maillage.</span><span class="sxs-lookup"><span data-stu-id="99008-104">Gets the mesh index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="99008-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99008-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="99008-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99008-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99008-107">*ppIB* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="99008-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="99008-108">Type : **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="99008-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="99008-109">Pointeur vers la mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="99008-109">Pointer to the index buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99008-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99008-110">Return value</span></span>

<span data-ttu-id="99008-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99008-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99008-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99008-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="99008-113">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="99008-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="99008-114">Notes</span><span class="sxs-lookup"><span data-stu-id="99008-114">Remarks</span></span>

<span data-ttu-id="99008-115">Le tampon d’index contient l’ordonnancement des vertex dans la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="99008-115">The index buffer contains the vertex ordering in the vertex buffer.</span></span> <span data-ttu-id="99008-116">Le tampon d’index est utilisé pour accéder à la mémoire tampon de vertex lorsque le maillage est rendu.</span><span class="sxs-lookup"><span data-stu-id="99008-116">The index buffer is used to access the vertex buffer when the mesh is rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="99008-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99008-117">Requirements</span></span>



| <span data-ttu-id="99008-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99008-118">Requirement</span></span> | <span data-ttu-id="99008-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="99008-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99008-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="99008-120">Header</span></span><br/>  | <dl> <span data-ttu-id="99008-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="99008-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="99008-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="99008-122">Library</span></span><br/> | <dl> <span data-ttu-id="99008-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99008-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="99008-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99008-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99008-125">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="99008-125">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
