---
description: 'ID3DXBaseMesh :: GetFVF, méthode-obtient la valeur du vertex de fonction fixe.'
ms.assetid: ed56ff2d-0366-426c-9f9a-7d1a7c5d1a7c
title: 'ID3DXBaseMesh :: GetFVF, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4e37db51238137d67ba6e060ecfafb7d1361727e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115437"
---
# <a name="id3dxbasemeshgetfvf-method"></a><span data-ttu-id="ef4f3-103">ID3DXBaseMesh :: GetFVF, méthode</span><span class="sxs-lookup"><span data-stu-id="ef4f3-103">ID3DXBaseMesh::GetFVF method</span></span>

<span data-ttu-id="ef4f3-104">Obtient la valeur de vertex de fonction fixe.</span><span class="sxs-lookup"><span data-stu-id="ef4f3-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef4f3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef4f3-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="ef4f3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef4f3-106">Parameters</span></span>

<span data-ttu-id="ef4f3-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ef4f3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ef4f3-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ef4f3-108">Return value</span></span>

<span data-ttu-id="ef4f3-109">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef4f3-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ef4f3-110">Retourne les codes de format de vertex flexible.</span><span class="sxs-lookup"><span data-stu-id="ef4f3-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef4f3-111">Notes </span><span class="sxs-lookup"><span data-stu-id="ef4f3-111">Remarks</span></span>

<span data-ttu-id="ef4f3-112">Cette méthode peut retourner 0 si le format du vertex ne peut pas être mappé directement à un code de la Commission.</span><span class="sxs-lookup"><span data-stu-id="ef4f3-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="ef4f3-113">Cela se produit pour un maillage créé à partir d’une déclaration de vertex qui n’a pas le même ordre et les mêmes éléments que ceux pris en charge par les codes de la Commission.</span><span class="sxs-lookup"><span data-stu-id="ef4f3-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef4f3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef4f3-114">Requirements</span></span>



| <span data-ttu-id="ef4f3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef4f3-115">Requirement</span></span> | <span data-ttu-id="ef4f3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef4f3-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef4f3-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef4f3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ef4f3-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef4f3-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ef4f3-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ef4f3-119">Library</span></span><br/> | <dl> <span data-ttu-id="ef4f3-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef4f3-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ef4f3-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef4f3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef4f3-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="ef4f3-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
