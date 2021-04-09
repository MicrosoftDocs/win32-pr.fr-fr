---
description: Définit si le mode de pavage actuel est discret ou continu.
ms.assetid: d8055a25-6a8e-4018-a993-762f6f0e0cd3
title: Énumération D3DPATCHEDGESTYLE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPATCHEDGESTYLE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e625b7c4ff12f9859efdcc2b10b551a2223adab6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870130"
---
# <a name="d3dpatchedgestyle-enumeration"></a><span data-ttu-id="c35bb-103">Énumération D3DPATCHEDGESTYLE</span><span class="sxs-lookup"><span data-stu-id="c35bb-103">D3DPATCHEDGESTYLE enumeration</span></span>

<span data-ttu-id="c35bb-104">Définit si le mode de pavage actuel est discret ou continu.</span><span class="sxs-lookup"><span data-stu-id="c35bb-104">Defines whether the current tessellation mode is discrete or continuous.</span></span>

## <a name="syntax"></a><span data-ttu-id="c35bb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c35bb-105">Syntax</span></span>


```C++
typedef enum D3DPATCHEDGESTYLE { 
  D3DPATCHEDGE_DISCRETE     = 0,
  D3DPATCHEDGE_CONTINUOUS   = 1,
  D3DPATCHEDGE_FORCE_DWORD  = 0x7fffffff
} D3DPATCHEDGESTYLE, *LPD3DPATCHEDGESTYLE;
```



## <a name="constants"></a><span data-ttu-id="c35bb-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c35bb-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c35bb-107"><span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE \_ discret**</span><span class="sxs-lookup"><span data-stu-id="c35bb-107"><span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE\_DISCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="c35bb-108">Style de contour discret.</span><span class="sxs-lookup"><span data-stu-id="c35bb-108">Discrete edge style.</span></span> <span data-ttu-id="c35bb-109">En mode discret, vous pouvez spécifier la facettisation float, mais elle sera tronquée en entiers.</span><span class="sxs-lookup"><span data-stu-id="c35bb-109">In discrete mode, you can specify float tessellation but it will be truncated to integers.</span></span>

</dd> <dt>

<span data-ttu-id="c35bb-110"><span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE \_ continu**</span><span class="sxs-lookup"><span data-stu-id="c35bb-110"><span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE\_CONTINUOUS**</span></span>
</dt> <dd>

<span data-ttu-id="c35bb-111">Style de périphérie continue.</span><span class="sxs-lookup"><span data-stu-id="c35bb-111">Continuous edge style.</span></span> <span data-ttu-id="c35bb-112">En mode continu, la facettisation est spécifiée en tant que valeurs float qui peuvent être modifiées facilement pour réduire les artefacts « dépilés ».</span><span class="sxs-lookup"><span data-stu-id="c35bb-112">In continuous mode, tessellation is specified as float values that can be smoothly varied to reduce "popping" artifacts.</span></span>

</dd> <dt>

<span data-ttu-id="c35bb-113"><span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c35bb-113"><span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="c35bb-114">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="c35bb-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="c35bb-115">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c35bb-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="c35bb-116">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c35bb-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c35bb-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c35bb-117">Remarks</span></span>

<span data-ttu-id="c35bb-118">Notez que le pavage continu produit un modèle de pavage complètement différent de celui de la même polygonalisation (ce qui est plus apparent en mode filaire).</span><span class="sxs-lookup"><span data-stu-id="c35bb-118">Note that continuous tessellation produces a completely different tessellation pattern from the discrete one for the same tessellation values (this is more apparent in wireframe mode).</span></span> <span data-ttu-id="c35bb-119">Ainsi, 4,0 Continuous n’est pas le même que 4 discret.</span><span class="sxs-lookup"><span data-stu-id="c35bb-119">Thus, 4.0 continuous is not the same as 4 discrete.</span></span>

## <a name="requirements"></a><span data-ttu-id="c35bb-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c35bb-120">Requirements</span></span>



| <span data-ttu-id="c35bb-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c35bb-121">Requirement</span></span> | <span data-ttu-id="c35bb-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c35bb-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c35bb-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c35bb-123">Header</span></span><br/> | <dl> <span data-ttu-id="c35bb-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c35bb-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c35bb-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c35bb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c35bb-126">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="c35bb-126">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




