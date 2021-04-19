---
description: Obtient le nombre de vertex dans la maille.
ms.assetid: fea8a3b5-ca10-4066-b2ca-6579829d31b6
title: 'ID3DX10Mesh :: GetVertexCount, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 189be6ff6872cfb85c2f336c29dedef2e435382e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535828"
---
# <a name="id3dx10meshgetvertexcount-method"></a><span data-ttu-id="768be-103">ID3DX10Mesh :: GetVertexCount, méthode</span><span class="sxs-lookup"><span data-stu-id="768be-103">ID3DX10Mesh::GetVertexCount method</span></span>

<span data-ttu-id="768be-104">Obtient le nombre de vertex dans la maille.</span><span class="sxs-lookup"><span data-stu-id="768be-104">Get the number of vertices in the mesh.</span></span> <span data-ttu-id="768be-105">Un maillage peut contenir plusieurs mémoires tampons de vertex (c’est-à-dire qu’une mémoire tampon de vertex peut contenir toutes les données de position, une autre peut contenir toutes les données de coordonnée de texture, etc.), mais chaque mémoire tampon de vertex contiendra le même nombre d’éléments.</span><span class="sxs-lookup"><span data-stu-id="768be-105">A mesh may contain multiple vertex buffers (i.e. one vertex buffer may contain all position data, another may contains all texture coordinate data, etc.), however each vertex buffer will contain the same number of elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="768be-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="768be-106">Syntax</span></span>


```C++
UINT GetVertexCount();
```



## <a name="parameters"></a><span data-ttu-id="768be-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="768be-107">Parameters</span></span>

<span data-ttu-id="768be-108">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="768be-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="768be-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="768be-109">Return value</span></span>

<span data-ttu-id="768be-110">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="768be-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="768be-111">Nombre de vertex dans la maille.</span><span class="sxs-lookup"><span data-stu-id="768be-111">The number of vertices in the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="768be-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="768be-112">Requirements</span></span>



| <span data-ttu-id="768be-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="768be-113">Requirement</span></span> | <span data-ttu-id="768be-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="768be-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="768be-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="768be-115">Header</span></span><br/>  | <dl> <span data-ttu-id="768be-116"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="768be-116"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="768be-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="768be-117">Library</span></span><br/> | <dl> <span data-ttu-id="768be-118"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="768be-118"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="768be-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="768be-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="768be-120">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="768be-120">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="768be-121">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="768be-121">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
