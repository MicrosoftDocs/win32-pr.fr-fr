---
description: Retourne la taille d’un vertex à partir de la déclaration de vertex.
ms.assetid: a2524f96-103e-43ab-bdcb-b99e7402fd89
title: D3DXGetDeclVertexSize, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c962064faa61dc7045b0111c5efbf1d1bea9fd40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524856"
---
# <a name="d3dxgetdeclvertexsize-function"></a><span data-ttu-id="e7841-103">D3DXGetDeclVertexSize fonction)</span><span class="sxs-lookup"><span data-stu-id="e7841-103">D3DXGetDeclVertexSize function</span></span>

<span data-ttu-id="e7841-104">Retourne la taille d’un vertex à partir de la déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="e7841-104">Returns the size of a vertex from the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7841-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7841-105">Syntax</span></span>


```C++
UINT D3DXGetDeclVertexSize(
  _In_ const D3DVERTEXELEMENT9 *pDecl,
  _In_       DWORD             Stream
);
```



## <a name="parameters"></a><span data-ttu-id="e7841-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7841-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7841-107">*pDecl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7841-107">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7841-108">Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="e7841-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="e7841-109">Pointeur vers la déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="e7841-109">A pointer to the vertex declaration.</span></span> <span data-ttu-id="e7841-110">Consultez [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="e7841-110">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7841-111">*Flux* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="e7841-111">*Stream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7841-112">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7841-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7841-113">Index de flux de base zéro.</span><span class="sxs-lookup"><span data-stu-id="e7841-113">The zero-based stream index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7841-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7841-114">Return value</span></span>

<span data-ttu-id="e7841-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7841-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7841-116">Taille de la déclaration de vertex, en octets.</span><span class="sxs-lookup"><span data-stu-id="e7841-116">The vertex declaration size, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7841-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7841-117">Requirements</span></span>



| <span data-ttu-id="e7841-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7841-118">Requirement</span></span> | <span data-ttu-id="e7841-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7841-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7841-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7841-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e7841-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7841-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e7841-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e7841-122">Library</span></span><br/> | <dl> <span data-ttu-id="e7841-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7841-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e7841-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7841-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7841-125">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="e7841-125">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
