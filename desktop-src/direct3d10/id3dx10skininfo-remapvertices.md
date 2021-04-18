---
description: Modifiez les vertex qui sont influencés par les segments.
ms.assetid: b0d71f3e-9a2d-469d-808b-2fa768cf14b0
title: 'ID3DX10SkinInfo :: RemapVertices, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cc51c912794135b456542bb9a8a779601681f393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106536246"
---
# <a name="id3dx10skininforemapvertices-method"></a><span data-ttu-id="b8c9c-103">ID3DX10SkinInfo :: RemapVertices, méthode</span><span class="sxs-lookup"><span data-stu-id="b8c9c-103">ID3DX10SkinInfo::RemapVertices method</span></span>

<span data-ttu-id="b8c9c-104">Modifiez les vertex qui sont influencés par les segments.</span><span class="sxs-lookup"><span data-stu-id="b8c9c-104">Change which vertices are influenced by which bones.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8c9c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8c9c-105">Syntax</span></span>


```C++
HRESULT RemapVertices(
  [in] UINT NewVertexCount,
  [in] UINT *pVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="b8c9c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8c9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8c9c-107">*NewVertexCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8c9c-107">*NewVertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8c9c-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8c9c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8c9c-109">Nouveau nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="b8c9c-109">The new number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="b8c9c-110">*pVertexRemap* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8c9c-110">*pVertexRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8c9c-111">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b8c9c-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b8c9c-112">Pointeur vers un tableau d’index de vertex qui décrivent le remappage.</span><span class="sxs-lookup"><span data-stu-id="b8c9c-112">A pointer to an array of vertex indices, which describe the remapping.</span></span> <span data-ttu-id="b8c9c-113">Par exemple, disons SkinInfo contient des vertex tels que bone0 est mappé à v0, bone1 à v1 et bone2 à v2, et Array avec 2, 1, 0 est spécifié pour pBoneRemap.</span><span class="sxs-lookup"><span data-stu-id="b8c9c-113">For example, say SkinInfo contains some vertices such that bone0 is mapped to v0, bone1 to v1, and bone2 to v2, and array with 2,1,0 is specified for pBoneRemap.</span></span> <span data-ttu-id="b8c9c-114">Bone0 sera alors mappé à v2, bone1 à v1 et bone2 à v0.</span><span class="sxs-lookup"><span data-stu-id="b8c9c-114">This will cause bone0 to be mapped to v2, bone1 to v1, and bone2 to v0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8c9c-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b8c9c-115">Return value</span></span>

<span data-ttu-id="b8c9c-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b8c9c-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b8c9c-117">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b8c9c-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b8c9c-118">Si la méthode échoue, la valeur de retour peut être : E \_ OUTOFMEMORY ou e \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="b8c9c-118">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8c9c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8c9c-119">Requirements</span></span>



| <span data-ttu-id="b8c9c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8c9c-120">Requirement</span></span> | <span data-ttu-id="b8c9c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8c9c-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8c9c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8c9c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b8c9c-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8c9c-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b8c9c-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b8c9c-124">Library</span></span><br/> | <dl> <span data-ttu-id="b8c9c-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8c9c-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8c9c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8c9c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8c9c-127">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="b8c9c-127">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="b8c9c-128">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="b8c9c-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
