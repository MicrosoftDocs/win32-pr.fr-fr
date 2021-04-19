---
description: Applique les enveloppes logicielles aux vertex cibles en fonction des matrices actuelles.
ms.assetid: 4858dfd4-dc0d-4852-9165-8ae1b40386d4
title: 'ID3DXSkinInfo :: UpdateSkinnedMesh, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.UpdateSkinnedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 645e6ae1e1cb84991b352c250b137cd3ae2491f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532415"
---
# <a name="id3dxskininfoupdateskinnedmesh-method"></a><span data-ttu-id="fb0a1-103">ID3DXSkinInfo :: UpdateSkinnedMesh, méthode</span><span class="sxs-lookup"><span data-stu-id="fb0a1-103">ID3DXSkinInfo::UpdateSkinnedMesh method</span></span>

<span data-ttu-id="fb0a1-104">Applique les enveloppes logicielles aux vertex cibles en fonction des matrices actuelles.</span><span class="sxs-lookup"><span data-stu-id="fb0a1-104">Applies software skinning to the target vertices based on the current matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb0a1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb0a1-105">Syntax</span></span>


```C++
HRESULT UpdateSkinnedMesh(
  [in] const D3DXMATRIX *pBoneTransforms,
  [in] const D3DXMATRIX *pBoneInvTransposeTransforms,
  [in]       LPCVOID    pVerticesSrc,
  [in]       PVOID      pVerticesDst
);
```



## <a name="parameters"></a><span data-ttu-id="fb0a1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb0a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb0a1-107">*pBoneTransforms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb0a1-107">*pBoneTransforms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb0a1-108">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fb0a1-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fb0a1-109">Matrice de transformation osseuse.</span><span class="sxs-lookup"><span data-stu-id="fb0a1-109">Bone transform matrix.</span></span>

</dd> <dt>

<span data-ttu-id="fb0a1-110">*pBoneInvTransposeTransforms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb0a1-110">*pBoneInvTransposeTransforms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb0a1-111">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fb0a1-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fb0a1-112">Transposer l’inverse de la matrice de transformation osseuse.</span><span class="sxs-lookup"><span data-stu-id="fb0a1-112">Inverse transpose of the bone transform matrix.</span></span>

</dd> <dt>

<span data-ttu-id="fb0a1-113">*pVerticesSrc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb0a1-113">*pVerticesSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb0a1-114">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb0a1-114">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb0a1-115">Pointeur vers la mémoire tampon qui contient les vertex sources.</span><span class="sxs-lookup"><span data-stu-id="fb0a1-115">Pointer to the buffer containing the source vertices.</span></span>

</dd> <dt>

<span data-ttu-id="fb0a1-116">*pVerticesDst* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb0a1-116">*pVerticesDst* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb0a1-117">Type : **[ **pVoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb0a1-117">Type: **[**PVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb0a1-118">Pointeur vers la mémoire tampon qui contient les sommets de destination.</span><span class="sxs-lookup"><span data-stu-id="fb0a1-118">Pointer to the buffer containing the destination vertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb0a1-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb0a1-119">Return value</span></span>

<span data-ttu-id="fb0a1-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb0a1-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb0a1-121">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fb0a1-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fb0a1-122">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fb0a1-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb0a1-123">Notes</span><span class="sxs-lookup"><span data-stu-id="fb0a1-123">Remarks</span></span>

<span data-ttu-id="fb0a1-124">Lorsqu’elle est utilisée pour l’apparence des vertex avec deux éléments de position, cette méthode enveloppe le deuxième élément de position avec l’inverse du segment au lieu du segment lui-même.</span><span class="sxs-lookup"><span data-stu-id="fb0a1-124">When used to skin vertices with two position elements, this method skins the second position element with the inverse of the bone instead of the bone itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb0a1-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb0a1-125">Requirements</span></span>



| <span data-ttu-id="fb0a1-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb0a1-126">Requirement</span></span> | <span data-ttu-id="fb0a1-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb0a1-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb0a1-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb0a1-128">Header</span></span><br/>  | <dl> <span data-ttu-id="fb0a1-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb0a1-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fb0a1-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fb0a1-130">Library</span></span><br/> | <dl> <span data-ttu-id="fb0a1-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb0a1-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fb0a1-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb0a1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb0a1-133">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="fb0a1-133">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
