---
description: Déverrouillez la mémoire tampon d’index.
ms.assetid: de3d0893-1596-42df-b049-6574c58ffa8d
title: 'ID3DXPatchMesh :: UnlockIndexBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9bae54c6c4477682422328410558f1b405eb2677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538973"
---
# <a name="id3dxpatchmeshunlockindexbuffer-method"></a><span data-ttu-id="d766e-103">ID3DXPatchMesh :: UnlockIndexBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="d766e-103">ID3DXPatchMesh::UnlockIndexBuffer method</span></span>

<span data-ttu-id="d766e-104">Déverrouillez la mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="d766e-104">Unlock the index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d766e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d766e-105">Syntax</span></span>


```C++
HRESULT UnlockIndexBuffer();
```



## <a name="parameters"></a><span data-ttu-id="d766e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d766e-106">Parameters</span></span>

<span data-ttu-id="d766e-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d766e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d766e-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d766e-108">Return value</span></span>

<span data-ttu-id="d766e-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d766e-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d766e-110">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d766e-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d766e-111">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d766e-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d766e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d766e-112">Remarks</span></span>

<span data-ttu-id="d766e-113">La mémoire tampon d’index est généralement verrouillée, écrite dans, puis déverrouillée pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="d766e-113">The index buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="d766e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d766e-114">Requirements</span></span>



| <span data-ttu-id="d766e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d766e-115">Requirement</span></span> | <span data-ttu-id="d766e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d766e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d766e-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="d766e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d766e-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d766e-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d766e-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d766e-119">Library</span></span><br/> | <dl> <span data-ttu-id="d766e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d766e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d766e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d766e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d766e-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="d766e-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




