---
description: Accédez à la mémoire tampon d’attribut du maillage.
ms.assetid: 01ebb592-1e0d-4d93-b3f5-ad5f1e0225d0
title: 'ID3DX10Mesh :: GetAttributeBuffer, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 161711cd28dae790fd25ff8dd192945a366e9dd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525897"
---
# <a name="id3dx10meshgetattributebuffer-method"></a><span data-ttu-id="b143b-103">ID3DX10Mesh :: GetAttributeBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="b143b-103">ID3DX10Mesh::GetAttributeBuffer method</span></span>

<span data-ttu-id="b143b-104">Accédez à la mémoire tampon d’attribut du maillage.</span><span class="sxs-lookup"><span data-stu-id="b143b-104">Access the mesh's attribute buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b143b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b143b-105">Syntax</span></span>


```C++
HRESULT GetAttributeBuffer(
  [out] ID3DX10MeshBuffer **ppAttributeBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="b143b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b143b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b143b-107">*ppAttributeBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b143b-107">*ppAttributeBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b143b-108">Type : **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b143b-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="b143b-109">Mémoire tampon d’attribut.</span><span class="sxs-lookup"><span data-stu-id="b143b-109">The attribute buffer.</span></span> <span data-ttu-id="b143b-110">Consultez [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="b143b-110">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b143b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b143b-111">Return value</span></span>

<span data-ttu-id="b143b-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b143b-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b143b-113">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b143b-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b143b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b143b-114">Requirements</span></span>



| <span data-ttu-id="b143b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b143b-115">Requirement</span></span> | <span data-ttu-id="b143b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b143b-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b143b-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="b143b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b143b-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b143b-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b143b-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b143b-119">Library</span></span><br/> | <dl> <span data-ttu-id="b143b-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b143b-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b143b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b143b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b143b-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="b143b-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="b143b-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="b143b-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




