---
description: Retourne la taille d’un vertex pour un format de vertex flexible.
ms.assetid: 9d8e2b1f-0ec8-46ab-8492-2cadd700225e
title: D3DXGetFVFVertexSize, fonction (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetFVFVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd5dbe5a58faf385d6f9f50f2fcb4a01a7c01dc5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545280"
---
# <a name="d3dxgetfvfvertexsize-function"></a><span data-ttu-id="693b9-103">D3DXGetFVFVertexSize fonction)</span><span class="sxs-lookup"><span data-stu-id="693b9-103">D3DXGetFVFVertexSize function</span></span>

<span data-ttu-id="693b9-104">Retourne la taille d’un vertex pour un format de vertex flexible.</span><span class="sxs-lookup"><span data-stu-id="693b9-104">Returns the size of a vertex for a flexible vertex format (FVF).</span></span>

## <a name="syntax"></a><span data-ttu-id="693b9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="693b9-105">Syntax</span></span>


```C++
UINT D3DXGetFVFVertexSize(
  _In_ DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="693b9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="693b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="693b9-107">*Commission* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="693b9-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="693b9-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="693b9-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="693b9-109">Commission de la Commission à interroger.</span><span class="sxs-lookup"><span data-stu-id="693b9-109">FVF to be queried.</span></span> <span data-ttu-id="693b9-110">Combinaison de [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="693b9-110">A combination of [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="693b9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="693b9-111">Return value</span></span>

<span data-ttu-id="693b9-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="693b9-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="693b9-113">Taille du vertex du prix de la Commission, en octets.</span><span class="sxs-lookup"><span data-stu-id="693b9-113">The FVF vertex size, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="693b9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="693b9-114">Requirements</span></span>



| <span data-ttu-id="693b9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="693b9-115">Requirement</span></span> | <span data-ttu-id="693b9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="693b9-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="693b9-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="693b9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="693b9-118"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="693b9-118"><dt>D3dx9mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="693b9-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="693b9-119">Library</span></span><br/> | <dl> <span data-ttu-id="693b9-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="693b9-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="693b9-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="693b9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="693b9-122">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="693b9-122">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
