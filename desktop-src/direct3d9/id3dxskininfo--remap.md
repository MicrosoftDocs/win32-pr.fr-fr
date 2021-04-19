---
description: Met à jour les informations d’influence osseuse pour qu’elles correspondent aux sommets après leur réorganisation. Cette méthode doit être appelée si la mémoire tampon de vertex cible a été réorganisée en externe.
ms.assetid: bff5229f-e547-4ab3-84c6-58b15a7825e9
title: 'ID3DXSkinInfo :: remapper, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Remap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 657cf0977592a8e19e68b8aeb950c62d404e7cdb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545258"
---
# <a name="id3dxskininforemap-method"></a><span data-ttu-id="21bf2-104">ID3DXSkinInfo :: remapper, méthode</span><span class="sxs-lookup"><span data-stu-id="21bf2-104">ID3DXSkinInfo::Remap method</span></span>

<span data-ttu-id="21bf2-105">Met à jour les informations d’influence osseuse pour qu’elles correspondent aux sommets après leur réorganisation.</span><span class="sxs-lookup"><span data-stu-id="21bf2-105">Updates bone influence information to match vertices after they are reordered.</span></span> <span data-ttu-id="21bf2-106">Cette méthode doit être appelée si la mémoire tampon de vertex cible a été réorganisée en externe.</span><span class="sxs-lookup"><span data-stu-id="21bf2-106">This method should be called if the target vertex buffer has been reordered externally.</span></span>

## <a name="syntax"></a><span data-ttu-id="21bf2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21bf2-107">Syntax</span></span>


```C++
HRESULT Remap(
  [in] DWORD NumVertices,
  [in] DWORD *pVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="21bf2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21bf2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21bf2-109">*NumVertices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="21bf2-109">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21bf2-110">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21bf2-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21bf2-111">Nombre de vertex à remapper.</span><span class="sxs-lookup"><span data-stu-id="21bf2-111">Number of vertices to remap.</span></span>

</dd> <dt>

<span data-ttu-id="21bf2-112">*pVertexRemap* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="21bf2-112">*pVertexRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21bf2-113">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="21bf2-113">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="21bf2-114">Tableau de DWORDs dont la longueur est spécifiée par NumVertices.</span><span class="sxs-lookup"><span data-stu-id="21bf2-114">Array of DWORDS whose length is specified by NumVertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21bf2-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21bf2-115">Return value</span></span>

<span data-ttu-id="21bf2-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21bf2-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21bf2-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="21bf2-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="21bf2-118">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="21bf2-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="21bf2-119">Notes</span><span class="sxs-lookup"><span data-stu-id="21bf2-119">Remarks</span></span>

<span data-ttu-id="21bf2-120">Chaque élément dans pVertexRemap spécifie l’index de vertex précédent pour cette position.</span><span class="sxs-lookup"><span data-stu-id="21bf2-120">Each element in pVertexRemap specifies the previous vertex index for that position.</span></span> <span data-ttu-id="21bf2-121">Par exemple, si un vertex était à la position 3 mais a été remappé à la position 5, le cinquième élément de pVertexRemap doit contenir 3.</span><span class="sxs-lookup"><span data-stu-id="21bf2-121">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap should contain 3.</span></span> <span data-ttu-id="21bf2-122">Le tableau de remappage de vertex retourné par [**ID3DXMesh :: Optimize**](id3dxmesh--optimize.md) peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="21bf2-122">The vertex remap array returned by [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) can be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="21bf2-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21bf2-123">Requirements</span></span>



| <span data-ttu-id="21bf2-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21bf2-124">Requirement</span></span> | <span data-ttu-id="21bf2-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="21bf2-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21bf2-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="21bf2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="21bf2-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="21bf2-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="21bf2-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="21bf2-128">Library</span></span><br/> | <dl> <span data-ttu-id="21bf2-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21bf2-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="21bf2-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21bf2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21bf2-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="21bf2-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
