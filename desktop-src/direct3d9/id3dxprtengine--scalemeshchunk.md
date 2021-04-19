---
description: Met à l’échelle tous les échantillons associés à un sous-maillage donné. La méthode est utile pour le calcul de la diffusion sous-surface.
ms.assetid: abb9ca6a-5fc2-4986-8a38-29998fe5e537
title: 'ID3DXPRTEngine :: ScaleMeshChunk, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ScaleMeshChunk
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f688a5175e7b50c33dd93d06a4f988a14c062c86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538065"
---
# <a name="id3dxprtenginescalemeshchunk-method"></a><span data-ttu-id="dadae-104">ID3DXPRTEngine :: ScaleMeshChunk, méthode</span><span class="sxs-lookup"><span data-stu-id="dadae-104">ID3DXPRTEngine::ScaleMeshChunk method</span></span>

<span data-ttu-id="dadae-105">Met à l’échelle tous les échantillons associés à un sous-maillage donné.</span><span class="sxs-lookup"><span data-stu-id="dadae-105">Scales all the samples associated with a given submesh.</span></span> <span data-ttu-id="dadae-106">La méthode est utile pour le calcul de la diffusion sous-surface.</span><span class="sxs-lookup"><span data-stu-id="dadae-106">The method is useful for computing subsurface scattering.</span></span>

## <a name="syntax"></a><span data-ttu-id="dadae-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dadae-107">Syntax</span></span>


```C++
HRESULT ScaleMeshChunk(
  [in]      UINT            uMeshChunk,
  [in]      FLOAT           fScale,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="dadae-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dadae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dadae-109">*uMeshChunk* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dadae-109">*uMeshChunk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadae-110">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dadae-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dadae-111">Emplacement dans la maille auquel démarrer les exemples de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="dadae-111">Location in the mesh at which to start scaling samples.</span></span>

</dd> <dt>

<span data-ttu-id="dadae-112">*fScale* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dadae-112">*fScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadae-113">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dadae-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dadae-114">Valeur par laquelle multiplier chaque vecteur dans le sous-maillage.</span><span class="sxs-lookup"><span data-stu-id="dadae-114">Value by which to multiply each vector in the submesh.</span></span>

</dd> <dt>

<span data-ttu-id="dadae-115">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dadae-115">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dadae-116">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="dadae-116">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="dadae-117">Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) pour recevoir des échantillons redimensionnés dans le sous-maillage.</span><span class="sxs-lookup"><span data-stu-id="dadae-117">Pointer to a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object to receive rescaled samples in the submesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dadae-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dadae-118">Return value</span></span>

<span data-ttu-id="dadae-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dadae-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dadae-120">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dadae-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="dadae-121">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="dadae-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="dadae-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dadae-122">Requirements</span></span>



| <span data-ttu-id="dadae-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dadae-123">Requirement</span></span> | <span data-ttu-id="dadae-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="dadae-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dadae-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="dadae-125">Header</span></span><br/>  | <dl> <span data-ttu-id="dadae-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dadae-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dadae-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dadae-127">Library</span></span><br/> | <dl> <span data-ttu-id="dadae-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dadae-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dadae-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dadae-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dadae-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="dadae-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
