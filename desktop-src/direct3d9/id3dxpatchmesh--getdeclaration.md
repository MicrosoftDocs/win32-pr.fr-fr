---
description: Obtient la déclaration de vertex.
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: 'ID3DXPatchMesh :: GetDeclaration, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d2d39192368fdca8ccaba7c51e64f60ea030568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323410"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a><span data-ttu-id="e22b4-103">ID3DXPatchMesh :: GetDeclaration, méthode</span><span class="sxs-lookup"><span data-stu-id="e22b4-103">ID3DXPatchMesh::GetDeclaration method</span></span>

<span data-ttu-id="e22b4-104">Obtient la déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="e22b4-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="e22b4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e22b4-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a><span data-ttu-id="e22b4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e22b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e22b4-107">*pDeclaration* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e22b4-107">*pDeclaration* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e22b4-108">Type : **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="e22b4-108">Type: **[**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="e22b4-109">Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) décrivant le format de vertex des vertex de maillage.</span><span class="sxs-lookup"><span data-stu-id="e22b4-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="e22b4-110">La dimension de ce tableau déclarateur est [**la \_ \_ \_ taille max Commission**](./max-fvf-decl-size.md)de la déclaration de la valeur.</span><span class="sxs-lookup"><span data-stu-id="e22b4-110">The dimension of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="e22b4-111">Le tableau d’éléments de vertex se termine par la macro [**\_ end D3DDECL**](d3ddecl-end.md) .</span><span class="sxs-lookup"><span data-stu-id="e22b4-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e22b4-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e22b4-112">Return value</span></span>

<span data-ttu-id="e22b4-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e22b4-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e22b4-114">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e22b4-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e22b4-115">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e22b4-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e22b4-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e22b4-116">Remarks</span></span>

<span data-ttu-id="e22b4-117">Le tableau d’éléments comprend la [**macro \_ end D3DDECL**](d3ddecl-end.md) , qui termine la déclaration.</span><span class="sxs-lookup"><span data-stu-id="e22b4-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="e22b4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e22b4-118">Requirements</span></span>



| <span data-ttu-id="e22b4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e22b4-119">Requirement</span></span> | <span data-ttu-id="e22b4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e22b4-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e22b4-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e22b4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e22b4-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e22b4-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e22b4-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e22b4-123">Library</span></span><br/> | <dl> <span data-ttu-id="e22b4-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e22b4-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e22b4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e22b4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e22b4-126">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="e22b4-126">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
