---
description: 'ID3DX10Mesh :: GetIndexBuffer, méthode-récupère les données dans une mémoire tampon d’index.'
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
ms.openlocfilehash: 751d6dd0376dc73f0213ddb83a19954dc154d633
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084027"
---
# <a name="id3dx10meshgetindexbuffer-method"></a><span data-ttu-id="96354-103">ID3DX10Mesh :: GetIndexBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="96354-103">ID3DX10Mesh::GetIndexBuffer method</span></span>

<span data-ttu-id="96354-104">Récupère les données dans une mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="96354-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="96354-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96354-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out] ID3DX10MeshBuffer **ppIndexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="96354-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96354-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96354-107">*ppIndexBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="96354-107">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96354-108">Type : **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="96354-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="96354-109">Adresse d’un pointeur vers une interface ID3DX10MeshBuffer, représentant la mémoire tampon d’index associée à la maille.</span><span class="sxs-lookup"><span data-stu-id="96354-109">Address of a pointer to a ID3DX10MeshBuffer interface, representing the index buffer associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96354-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="96354-110">Return value</span></span>

<span data-ttu-id="96354-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="96354-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="96354-112">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="96354-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="96354-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96354-113">Requirements</span></span>



| <span data-ttu-id="96354-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96354-114">Requirement</span></span> | <span data-ttu-id="96354-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="96354-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96354-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="96354-116">Header</span></span><br/>  | <dl> <span data-ttu-id="96354-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="96354-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="96354-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="96354-118">Library</span></span><br/> | <dl> <span data-ttu-id="96354-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96354-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96354-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96354-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96354-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="96354-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="96354-122">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="96354-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




