---
description: Déverrouillez la mémoire tampon de vertex.
ms.assetid: 98b82fd1-56e8-45f3-bf26-a1e3b54c2979
title: 'ID3DXPatchMesh :: UnlockVertexBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c6d4b6a55281048b303733e1addf2ab4636f74ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529641"
---
# <a name="id3dxpatchmeshunlockvertexbuffer-method"></a><span data-ttu-id="be676-103">ID3DXPatchMesh :: UnlockVertexBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="be676-103">ID3DXPatchMesh::UnlockVertexBuffer method</span></span>

<span data-ttu-id="be676-104">Déverrouillez la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="be676-104">Unlock the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="be676-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be676-105">Syntax</span></span>


```C++
HRESULT UnlockVertexBuffer();
```



## <a name="parameters"></a><span data-ttu-id="be676-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be676-106">Parameters</span></span>

<span data-ttu-id="be676-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="be676-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="be676-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be676-108">Return value</span></span>

<span data-ttu-id="be676-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="be676-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="be676-110">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="be676-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="be676-111">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="be676-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="be676-112">Notes</span><span class="sxs-lookup"><span data-stu-id="be676-112">Remarks</span></span>

<span data-ttu-id="be676-113">La mémoire tampon de vertex est généralement verrouillée, écrite dans, puis déverrouillée pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="be676-113">The vertex buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="be676-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be676-114">Requirements</span></span>



| <span data-ttu-id="be676-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be676-115">Requirement</span></span> | <span data-ttu-id="be676-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="be676-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be676-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="be676-117">Header</span></span><br/>  | <dl> <span data-ttu-id="be676-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="be676-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="be676-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="be676-119">Library</span></span><br/> | <dl> <span data-ttu-id="be676-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be676-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="be676-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be676-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be676-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="be676-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




