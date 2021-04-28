---
description: 'ID3DX10Mesh :: GetVertexBuffer, méthode-récupère la mémoire tampon de vertex associée à la maille.'
ms.assetid: c69a712b-8964-4a5b-a136-3f24060b7fd8
title: 'ID3DX10Mesh :: GetVertexBuffer, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a63b08cf978a65e1fa9999c79b8033436b41fa2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108077"
---
# <a name="id3dx10meshgetvertexbuffer-method"></a><span data-ttu-id="7773d-103">ID3DX10Mesh :: GetVertexBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="7773d-103">ID3DX10Mesh::GetVertexBuffer method</span></span>

<span data-ttu-id="7773d-104">Récupère la mémoire tampon de vertex associée à la maille.</span><span class="sxs-lookup"><span data-stu-id="7773d-104">Retrieves the vertex buffer associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="7773d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7773d-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [in]  UINT              iBuffer,
  [out] ID3DX10MeshBuffer **ppVertexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="7773d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7773d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7773d-107">*iBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7773d-107">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7773d-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7773d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7773d-109">Mémoire tampon de vertex à récupérer.</span><span class="sxs-lookup"><span data-stu-id="7773d-109">The vertex buffer to get.</span></span> <span data-ttu-id="7773d-110">Il s’agit d’une valeur d’index.</span><span class="sxs-lookup"><span data-stu-id="7773d-110">This is an index value.</span></span>

</dd> <dt>

<span data-ttu-id="7773d-111">*ppVertexBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7773d-111">*ppVertexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7773d-112">Type : **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="7773d-112">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="7773d-113">Mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="7773d-113">The vertex buffer.</span></span> <span data-ttu-id="7773d-114">Voir [ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="7773d-114">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7773d-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7773d-115">Return value</span></span>

<span data-ttu-id="7773d-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7773d-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7773d-117">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7773d-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7773d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7773d-118">Requirements</span></span>



| <span data-ttu-id="7773d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7773d-119">Requirement</span></span> | <span data-ttu-id="7773d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7773d-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7773d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="7773d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7773d-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7773d-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7773d-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7773d-123">Library</span></span><br/> | <dl> <span data-ttu-id="7773d-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7773d-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7773d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7773d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7773d-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="7773d-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="7773d-127">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="7773d-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
