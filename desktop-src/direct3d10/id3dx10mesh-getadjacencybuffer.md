---
description: Accédez à la mémoire tampon d’adjacence du maillage.
ms.assetid: 42b13f14-4edf-4b56-9198-60a548855542
title: 'ID3DX10Mesh :: GetAdjacencyBuffer, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAdjacencyBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 80dd5c6e6d9b12cb1c648c42a4758d215d3810c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535829"
---
# <a name="id3dx10meshgetadjacencybuffer-method"></a><span data-ttu-id="61851-103">ID3DX10Mesh :: GetAdjacencyBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="61851-103">ID3DX10Mesh::GetAdjacencyBuffer method</span></span>

<span data-ttu-id="61851-104">Accédez à la mémoire tampon d’adjacence du maillage.</span><span class="sxs-lookup"><span data-stu-id="61851-104">Access the mesh's adjacency buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="61851-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61851-105">Syntax</span></span>


```C++
HRESULT GetAdjacencyBuffer(
  [out] ID3DX10MeshBuffer **ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="61851-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61851-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61851-107">*ppAdjacency* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="61851-107">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61851-108">Type : **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="61851-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="61851-109">Mémoire tampon de contiguïté.</span><span class="sxs-lookup"><span data-stu-id="61851-109">The adjacency buffer.</span></span> <span data-ttu-id="61851-110">Consultez [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="61851-110">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61851-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61851-111">Return value</span></span>

<span data-ttu-id="61851-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="61851-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="61851-113">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="61851-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="61851-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61851-114">Requirements</span></span>



| <span data-ttu-id="61851-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61851-115">Requirement</span></span> | <span data-ttu-id="61851-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="61851-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61851-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="61851-117">Header</span></span><br/>  | <dl> <span data-ttu-id="61851-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="61851-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="61851-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="61851-119">Library</span></span><br/> | <dl> <span data-ttu-id="61851-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61851-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61851-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61851-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61851-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="61851-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="61851-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="61851-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




