---
description: Récupère les données dans une mémoire tampon d’index.
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
ms.openlocfilehash: 5b7cf57cd8f31e54cf48ae7f0cab69a40783debe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323041"
---
# <a name="id3dxbasemeshgetindexbuffer-method"></a><span data-ttu-id="e9f32-103">ID3DXBaseMesh :: GetIndexBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="e9f32-103">ID3DXBaseMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="e9f32-104">Récupère les données dans une mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="e9f32-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f32-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9f32-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="e9f32-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9f32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9f32-107">*ppIB* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e9f32-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f32-108">Type : **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="e9f32-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="e9f32-109">Adresse d’un pointeur vers une interface [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , représentant l’objet de mémoire tampon d’index associé à la maille.</span><span class="sxs-lookup"><span data-stu-id="e9f32-109">Address of a pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9f32-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9f32-110">Return value</span></span>

<span data-ttu-id="e9f32-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e9f32-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e9f32-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e9f32-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e9f32-113">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e9f32-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f32-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9f32-114">Requirements</span></span>



| <span data-ttu-id="e9f32-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9f32-115">Requirement</span></span> | <span data-ttu-id="e9f32-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9f32-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f32-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9f32-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e9f32-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9f32-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e9f32-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e9f32-119">Library</span></span><br/> | <dl> <span data-ttu-id="e9f32-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9f32-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e9f32-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9f32-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f32-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="e9f32-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
