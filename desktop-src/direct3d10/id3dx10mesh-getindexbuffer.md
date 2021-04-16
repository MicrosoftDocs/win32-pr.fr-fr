---
description: Récupère les données dans une mémoire tampon d’index.
ms.assetid: 7e25ad67-7f9d-4c23-a029-a2262034ef38
title: 'ID3DX10Mesh :: GetIndexBuffer, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c2777a9d530ac7217b1cc0f3c0f148998cc70ffe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394132"
---
# <a name="id3dx10meshgetindexbuffer-method"></a><span data-ttu-id="aa08c-103">ID3DX10Mesh :: GetIndexBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="aa08c-103">ID3DX10Mesh::GetIndexBuffer method</span></span>

<span data-ttu-id="aa08c-104">Récupère les données dans une mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="aa08c-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa08c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa08c-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out] ID3DX10MeshBuffer **ppIndexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="aa08c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa08c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa08c-107">*ppIndexBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="aa08c-107">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa08c-108">Type : **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="aa08c-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="aa08c-109">Adresse d’un pointeur vers une interface ID3DX10MeshBuffer, représentant la mémoire tampon d’index associée à la maille.</span><span class="sxs-lookup"><span data-stu-id="aa08c-109">Address of a pointer to a ID3DX10MeshBuffer interface, representing the index buffer associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa08c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aa08c-110">Return value</span></span>

<span data-ttu-id="aa08c-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aa08c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aa08c-112">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="aa08c-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa08c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa08c-113">Requirements</span></span>



| <span data-ttu-id="aa08c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa08c-114">Requirement</span></span> | <span data-ttu-id="aa08c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa08c-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa08c-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa08c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="aa08c-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa08c-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="aa08c-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aa08c-118">Library</span></span><br/> | <dl> <span data-ttu-id="aa08c-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa08c-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa08c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa08c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa08c-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="aa08c-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="aa08c-122">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="aa08c-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




