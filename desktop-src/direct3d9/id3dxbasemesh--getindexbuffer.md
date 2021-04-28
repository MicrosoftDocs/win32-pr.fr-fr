---
description: 'ID3DXBaseMesh :: GetIndexBuffer, méthode-récupère les données dans une mémoire tampon d’index.'
ms.assetid: 8e14a047-a8a6-4763-88c7-3b439044eeb4
title: 'ID3DXBaseMesh :: GetIndexBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 40e57193a2bf9a47ed0c57e6d13644441fbc42ce
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115427"
---
# <a name="id3dxbasemeshgetindexbuffer-method"></a><span data-ttu-id="bcba7-103">ID3DXBaseMesh :: GetIndexBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="bcba7-103">ID3DXBaseMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="bcba7-104">Récupère les données dans une mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="bcba7-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcba7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcba7-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="bcba7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bcba7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcba7-107">*ppIB* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bcba7-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bcba7-108">Type : **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="bcba7-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="bcba7-109">Adresse d’un pointeur vers une interface [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , représentant l’objet de mémoire tampon d’index associé à la maille.</span><span class="sxs-lookup"><span data-stu-id="bcba7-109">Address of a pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcba7-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bcba7-110">Return value</span></span>

<span data-ttu-id="bcba7-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bcba7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bcba7-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bcba7-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bcba7-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bcba7-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcba7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcba7-114">Requirements</span></span>



| <span data-ttu-id="bcba7-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcba7-115">Requirement</span></span> | <span data-ttu-id="bcba7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcba7-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcba7-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="bcba7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="bcba7-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcba7-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bcba7-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bcba7-119">Library</span></span><br/> | <dl> <span data-ttu-id="bcba7-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bcba7-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bcba7-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcba7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcba7-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="bcba7-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
