---
description: Mappe les index de la plage 0 à 255 aux États de transformation correspondants.
ms.assetid: b0a1548c-de5d-4eff-baf9-4aecb5e13443
title: Macro D3DTS_WORLDMATRIX (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDMATRIX
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f80996a37e2fb48bf8ca7ea73f714b04e711b263
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530874"
---
# <a name="d3dts_worldmatrix-macro"></a><span data-ttu-id="c38d6-103">D3DTS \_ macro WORLDMATRIX</span><span class="sxs-lookup"><span data-stu-id="c38d6-103">D3DTS\_WORLDMATRIX macro</span></span>

<span data-ttu-id="c38d6-104">Mappe les index de la plage 0 à 255 aux États de transformation correspondants.</span><span class="sxs-lookup"><span data-stu-id="c38d6-104">Maps indices in the range 0 through 255 to the corresponding transform states.</span></span>

## <a name="syntax"></a><span data-ttu-id="c38d6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c38d6-105">Syntax</span></span>


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLDMATRIX(
   int index
);
```



## <a name="parameters"></a><span data-ttu-id="c38d6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c38d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c38d6-107">*index*</span><span class="sxs-lookup"><span data-stu-id="c38d6-107">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="c38d6-108">Valeur d’index comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="c38d6-108">An index value in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c38d6-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c38d6-109">Return value</span></span>

<span data-ttu-id="c38d6-110">[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) mappé à l' *index* donné.</span><span class="sxs-lookup"><span data-stu-id="c38d6-110">The [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) that maps to the given *index*.</span></span>

## <a name="remarks"></a><span data-ttu-id="c38d6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c38d6-111">Remarks</span></span>

<span data-ttu-id="c38d6-112">Les États de transformation de la plage 256 à 511 sont réservés pour stocker jusqu’à 256 matrices qui peuvent être indexées à l’aide d’index 8 bits.</span><span class="sxs-lookup"><span data-stu-id="c38d6-112">Transform states in the range 256 through 511 are reserved to store up to 256 matrices that can be indexed using 8-bit indices.</span></span>

## <a name="requirements"></a><span data-ttu-id="c38d6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c38d6-113">Requirements</span></span>



| <span data-ttu-id="c38d6-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c38d6-114">Requirement</span></span> | <span data-ttu-id="c38d6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c38d6-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c38d6-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="c38d6-116">Header</span></span><br/> | <dl> <span data-ttu-id="c38d6-117"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c38d6-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c38d6-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c38d6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c38d6-119">Macros</span><span class="sxs-lookup"><span data-stu-id="c38d6-119">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="c38d6-120">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="c38d6-120">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 
