---
description: Obtient la valeur de vertex de fonction fixe.
ms.assetid: 9b80c4b9-2e5b-4965-99b9-ad6c459ef413
title: 'ID3DXSkinInfo :: GetFVF, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d48cd9cea6efd6cb43e6da6877a7aaf42909c71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322605"
---
# <a name="id3dxskininfogetfvf-method"></a><span data-ttu-id="09cfd-103">ID3DXSkinInfo :: GetFVF, méthode</span><span class="sxs-lookup"><span data-stu-id="09cfd-103">ID3DXSkinInfo::GetFVF method</span></span>

<span data-ttu-id="09cfd-104">Obtient la valeur de vertex de fonction fixe.</span><span class="sxs-lookup"><span data-stu-id="09cfd-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="09cfd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09cfd-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="09cfd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09cfd-106">Parameters</span></span>

<span data-ttu-id="09cfd-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="09cfd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="09cfd-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09cfd-108">Return value</span></span>

<span data-ttu-id="09cfd-109">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09cfd-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="09cfd-110">Retourne les codes de format de vertex flexible.</span><span class="sxs-lookup"><span data-stu-id="09cfd-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="09cfd-111">Notes</span><span class="sxs-lookup"><span data-stu-id="09cfd-111">Remarks</span></span>

<span data-ttu-id="09cfd-112">Cette méthode peut retourner 0 si le format du vertex ne peut pas être mappé directement à un code de la Commission.</span><span class="sxs-lookup"><span data-stu-id="09cfd-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="09cfd-113">Cela se produit pour un maillage créé à partir d’une déclaration de vertex qui n’a pas le même ordre et les mêmes éléments que ceux pris en charge par les codes de la Commission.</span><span class="sxs-lookup"><span data-stu-id="09cfd-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="09cfd-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09cfd-114">Requirements</span></span>



| <span data-ttu-id="09cfd-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09cfd-115">Requirement</span></span> | <span data-ttu-id="09cfd-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="09cfd-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09cfd-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="09cfd-117">Header</span></span><br/>  | <dl> <span data-ttu-id="09cfd-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="09cfd-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="09cfd-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="09cfd-119">Library</span></span><br/> | <dl> <span data-ttu-id="09cfd-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09cfd-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="09cfd-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09cfd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09cfd-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="09cfd-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="09cfd-123">**ID3DXSkinInfo::SetFVF**</span><span class="sxs-lookup"><span data-stu-id="09cfd-123">**ID3DXSkinInfo::SetFVF**</span></span>](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
