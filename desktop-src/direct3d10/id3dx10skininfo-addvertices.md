---
description: Allouez de l’espace pour des vertex supplémentaires.
ms.assetid: dd6445ea-4754-4ba3-a264-59295325ee08
title: 'ID3DX10SkinInfo :: AddVertices, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8f126b31c375e4e3463133960c5a1bcfbd995b62
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106533719"
---
# <a name="id3dx10skininfoaddvertices-method"></a><span data-ttu-id="ee6d5-103">ID3DX10SkinInfo :: AddVertices, méthode</span><span class="sxs-lookup"><span data-stu-id="ee6d5-103">ID3DX10SkinInfo::AddVertices method</span></span>

<span data-ttu-id="ee6d5-104">Allouez de l’espace pour des vertex supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ee6d5-104">Allocate space for additional vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee6d5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee6d5-105">Syntax</span></span>


```C++
HRESULT AddVertices(
  [in] UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="ee6d5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee6d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee6d5-107">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee6d5-107">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6d5-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee6d5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee6d5-109">Nombre de vertex à ajouter.</span><span class="sxs-lookup"><span data-stu-id="ee6d5-109">The number of vertices to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee6d5-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ee6d5-110">Return value</span></span>

<span data-ttu-id="ee6d5-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ee6d5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ee6d5-112">Si cette méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ee6d5-112">If this method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ee6d5-113">Si la méthode échoue, la valeur de retour peut être : E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ee6d5-113">If the method fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee6d5-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee6d5-114">Requirements</span></span>



| <span data-ttu-id="ee6d5-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee6d5-115">Requirement</span></span> | <span data-ttu-id="ee6d5-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee6d5-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee6d5-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee6d5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ee6d5-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee6d5-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ee6d5-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ee6d5-119">Library</span></span><br/> | <dl> <span data-ttu-id="ee6d5-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee6d5-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee6d5-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee6d5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee6d5-122">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="ee6d5-122">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="ee6d5-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="ee6d5-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
