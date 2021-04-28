---
description: 'ID3DXBaseMesh :: GetVertexBuffer, méthode-récupère la mémoire tampon de vertex associée à la maille.'
ms.assetid: 5caa6ce1-feab-4919-944e-f92fad3ad443
title: 'ID3DXBaseMesh :: GetVertexBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9533188e3e2effe1759b58f70c9f033cc491844c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115367"
---
# <a name="id3dxbasemeshgetvertexbuffer-method"></a><span data-ttu-id="042da-103">ID3DXBaseMesh :: GetVertexBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="042da-103">ID3DXBaseMesh::GetVertexBuffer method</span></span>

<span data-ttu-id="042da-104">Récupère la mémoire tampon de vertex associée à la maille.</span><span class="sxs-lookup"><span data-stu-id="042da-104">Retrieves the vertex buffer associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="042da-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="042da-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [out, retval] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a><span data-ttu-id="042da-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="042da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="042da-107">*ppVB* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="042da-107">*ppVB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="042da-108">Type : **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="042da-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span></span>

<span data-ttu-id="042da-109">Adresse d’un pointeur vers une interface [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) , représentant l’objet de mémoire tampon de vertex associé à la maille.</span><span class="sxs-lookup"><span data-stu-id="042da-109">Address of a pointer to an [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) interface, representing the vertex buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="042da-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="042da-110">Return value</span></span>

<span data-ttu-id="042da-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="042da-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="042da-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="042da-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="042da-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="042da-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="042da-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="042da-114">Requirements</span></span>



| <span data-ttu-id="042da-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="042da-115">Requirement</span></span> | <span data-ttu-id="042da-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="042da-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="042da-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="042da-117">Header</span></span><br/>  | <dl> <span data-ttu-id="042da-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="042da-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="042da-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="042da-119">Library</span></span><br/> | <dl> <span data-ttu-id="042da-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="042da-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="042da-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="042da-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="042da-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="042da-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
