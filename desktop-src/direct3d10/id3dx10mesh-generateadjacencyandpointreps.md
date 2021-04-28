---
description: 'ID3DX10Mesh :: GenerateAdjacencyAndPointReps, méthode-générer une liste de bords de maillage, ainsi qu’une liste des visages qui partagent chaque bord.'
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: 'ID3DX10Mesh :: GenerateAdjacencyAndPointReps, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateAdjacencyAndPointReps
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e496f96f36805d411c71e9aba1e2560b0dcbe3c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083977"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a><span data-ttu-id="eb7be-103">ID3DX10Mesh :: GenerateAdjacencyAndPointReps, méthode</span><span class="sxs-lookup"><span data-stu-id="eb7be-103">ID3DX10Mesh::GenerateAdjacencyAndPointReps method</span></span>

<span data-ttu-id="eb7be-104">Générez une liste de contours de maillage, ainsi qu’une liste des visages qui partagent chaque arête.</span><span class="sxs-lookup"><span data-stu-id="eb7be-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb7be-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb7be-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a><span data-ttu-id="eb7be-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb7be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb7be-107">*Epsilon* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb7be-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb7be-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb7be-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb7be-109">Spécifie que les vertex qui diffèrent de la position par moins de Epsilon doivent être traités comme coïncidents.</span><span class="sxs-lookup"><span data-stu-id="eb7be-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb7be-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eb7be-110">Return value</span></span>

<span data-ttu-id="eb7be-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eb7be-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eb7be-112">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="eb7be-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eb7be-113">Notes </span><span class="sxs-lookup"><span data-stu-id="eb7be-113">Remarks</span></span>

<span data-ttu-id="eb7be-114">Une fois qu’une application a généré des informations d’adjacence pour une maille, les données de maillage peuvent être optimisées pour améliorer les performances de dessin.</span><span class="sxs-lookup"><span data-stu-id="eb7be-114">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="eb7be-115">L’ordre des entrées dans la mémoire tampon d’adjacence est déterminé par l’ordre des index de vertex dans le tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="eb7be-115">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="eb7be-116">Le triangle adjacent 0 correspond toujours au bord entre les index des angles 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="eb7be-116">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="eb7be-117">Le triangle 1 adjacent correspond toujours au bord entre les index des angles 1 et 2, tandis que le triangle 2 adjacent correspond au bord entre les index des angles 2 et 0.</span><span class="sxs-lookup"><span data-stu-id="eb7be-117">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb7be-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb7be-118">Requirements</span></span>



| <span data-ttu-id="eb7be-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb7be-119">Requirement</span></span> | <span data-ttu-id="eb7be-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb7be-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb7be-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb7be-121">Header</span></span><br/>  | <dl> <span data-ttu-id="eb7be-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb7be-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb7be-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eb7be-123">Library</span></span><br/> | <dl> <span data-ttu-id="eb7be-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb7be-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb7be-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb7be-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb7be-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="eb7be-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="eb7be-127">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="eb7be-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
