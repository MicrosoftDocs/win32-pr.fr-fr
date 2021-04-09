---
description: Ajoute des données d’adjacence à la mémoire tampon d’index du maillage. Lorsque la maille doit être envoyée à un nuanceur Geometry qui accepte les données d’contiguïté, il est nécessaire que le tampon d’index du maillage contienne les données d’contiguïté.
ms.assetid: 8e587620-a4b6-4415-8fe7-9ec22f253b16
title: 'ID3DX10Mesh :: GenerateGSAdjacency, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateGSAdjacency
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d47747acfa97fbe843dabf527c8f94742db78d6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043138"
---
# <a name="id3dx10meshgenerategsadjacency-method"></a><span data-ttu-id="ef67a-104">ID3DX10Mesh :: GenerateGSAdjacency, méthode</span><span class="sxs-lookup"><span data-stu-id="ef67a-104">ID3DX10Mesh::GenerateGSAdjacency method</span></span>

<span data-ttu-id="ef67a-105">Ajoute des données d’adjacence à la mémoire tampon d’index du maillage.</span><span class="sxs-lookup"><span data-stu-id="ef67a-105">Adds adjacency data to the mesh's index buffer.</span></span> <span data-ttu-id="ef67a-106">Lorsque la maille doit être envoyée à un nuanceur Geometry qui accepte les données d’contiguïté, il est nécessaire que le tampon d’index du maillage contienne les données d’contiguïté.</span><span class="sxs-lookup"><span data-stu-id="ef67a-106">When the mesh is to be sent to a geometry shader that takes adjacency data, it is neccessary for the mesh's index buffer to contain adjacency data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef67a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef67a-107">Syntax</span></span>


```C++
HRESULT GenerateGSAdjacency();
```



## <a name="parameters"></a><span data-ttu-id="ef67a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef67a-108">Parameters</span></span>

<span data-ttu-id="ef67a-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ef67a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ef67a-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef67a-110">Return value</span></span>

<span data-ttu-id="ef67a-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ef67a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ef67a-112">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ef67a-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef67a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef67a-113">Requirements</span></span>



| <span data-ttu-id="ef67a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef67a-114">Requirement</span></span> | <span data-ttu-id="ef67a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef67a-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef67a-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef67a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ef67a-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef67a-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef67a-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ef67a-118">Library</span></span><br/> | <dl> <span data-ttu-id="ef67a-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef67a-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef67a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef67a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef67a-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="ef67a-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="ef67a-122">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="ef67a-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




