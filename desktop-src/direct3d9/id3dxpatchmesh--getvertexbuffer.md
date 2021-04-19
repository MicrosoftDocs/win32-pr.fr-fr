---
description: Obtient la mémoire tampon de vertex de maillage.
ms.assetid: 4ea4e99b-5c2c-467b-8b5d-8174c446680a
title: 'ID3DXPatchMesh :: GetVertexBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b8c3bb79d4c04db072adef857de195df7a0f0fff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531377"
---
# <a name="id3dxpatchmeshgetvertexbuffer-method"></a><span data-ttu-id="ad492-103">ID3DXPatchMesh :: GetVertexBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="ad492-103">ID3DXPatchMesh::GetVertexBuffer method</span></span>

<span data-ttu-id="ad492-104">Obtient la mémoire tampon de vertex de maillage.</span><span class="sxs-lookup"><span data-stu-id="ad492-104">Gets the mesh vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad492-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad492-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [out] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a><span data-ttu-id="ad492-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad492-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad492-107">*ppVB* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ad492-107">*ppVB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad492-108">Type : **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="ad492-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span></span>

<span data-ttu-id="ad492-109">Pointeur vers la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="ad492-109">Pointer to the vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad492-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad492-110">Return value</span></span>

<span data-ttu-id="ad492-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ad492-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ad492-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ad492-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ad492-113">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ad492-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad492-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ad492-114">Remarks</span></span>

<span data-ttu-id="ad492-115">Cette méthode suppose une polygonalisation uniforme.</span><span class="sxs-lookup"><span data-stu-id="ad492-115">This method assumes uniform tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad492-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad492-116">Requirements</span></span>



| <span data-ttu-id="ad492-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad492-117">Requirement</span></span> | <span data-ttu-id="ad492-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad492-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad492-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad492-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ad492-120"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad492-120"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ad492-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ad492-121">Library</span></span><br/> | <dl> <span data-ttu-id="ad492-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad492-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ad492-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad492-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad492-124">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="ad492-124">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
