---
description: Définit des constantes décrivant le mode de remplissage.
ms.assetid: be835432-e8d5-4afb-a810-2dac25bdc9dc
title: Énumération D3DFILLMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFILLMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 33cf03258933055aa18aecb42fffe4d8f33b1e51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531584"
---
# <a name="d3dfillmode-enumeration"></a><span data-ttu-id="2d433-103">Énumération D3DFILLMODE</span><span class="sxs-lookup"><span data-stu-id="2d433-103">D3DFILLMODE enumeration</span></span>

<span data-ttu-id="2d433-104">Définit des constantes décrivant le mode de remplissage.</span><span class="sxs-lookup"><span data-stu-id="2d433-104">Defines constants describing the fill mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d433-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d433-105">Syntax</span></span>


```C++
typedef enum D3DFILLMODE { 
  D3DFILL_POINT        = 1,
  D3DFILL_WIREFRAME    = 2,
  D3DFILL_SOLID        = 3,
  D3DFILL_FORCE_DWORD  = 0x7fffffff
} D3DFILLMODE, *LPD3DFILLMODE;
```



## <a name="constants"></a><span data-ttu-id="2d433-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="2d433-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2d433-107"><span id="D3DFILL_POINT"></span><span id="d3dfill_point"></span>**\_Point D3DFILL**</span><span class="sxs-lookup"><span data-stu-id="2d433-107"><span id="D3DFILL_POINT"></span><span id="d3dfill_point"></span>**D3DFILL\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="2d433-108">Points de remplissage.</span><span class="sxs-lookup"><span data-stu-id="2d433-108">Fill points.</span></span>

</dd> <dt>

<span data-ttu-id="2d433-109"><span id="D3DFILL_WIREFRAME"></span><span id="d3dfill_wireframe"></span>**D3DFILL \_ filaire**</span><span class="sxs-lookup"><span data-stu-id="2d433-109"><span id="D3DFILL_WIREFRAME"></span><span id="d3dfill_wireframe"></span>**D3DFILL\_WIREFRAME**</span></span>
</dt> <dd>

<span data-ttu-id="2d433-110">Remplissez des maquettes.</span><span class="sxs-lookup"><span data-stu-id="2d433-110">Fill wireframes.</span></span>

</dd> <dt>

<span data-ttu-id="2d433-111"><span id="D3DFILL_SOLID"></span><span id="d3dfill_solid"></span>**D3DFILL \_ Solid**</span><span class="sxs-lookup"><span data-stu-id="2d433-111"><span id="D3DFILL_SOLID"></span><span id="d3dfill_solid"></span>**D3DFILL\_SOLID**</span></span>
</dt> <dd>

<span data-ttu-id="2d433-112">Remplir des solides.</span><span class="sxs-lookup"><span data-stu-id="2d433-112">Fill solids.</span></span>

</dd> <dt>

<span data-ttu-id="2d433-113"><span id="D3DFILL_FORCE_DWORD"></span><span id="d3dfill_force_dword"></span>**D3DFILL \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2d433-113"><span id="D3DFILL_FORCE_DWORD"></span><span id="d3dfill_force_dword"></span>**D3DFILL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="2d433-114">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="2d433-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="2d433-115">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2d433-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="2d433-116">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2d433-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d433-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2d433-117">Remarks</span></span>

<span data-ttu-id="2d433-118">Les valeurs de ce type énuméré sont utilisées par l’état de \_ rendu D3DRS FillMode.</span><span class="sxs-lookup"><span data-stu-id="2d433-118">The values in this enumerated type are used by the D3DRS\_FILLMODE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d433-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d433-119">Requirements</span></span>



| <span data-ttu-id="2d433-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d433-120">Requirement</span></span> | <span data-ttu-id="2d433-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d433-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d433-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d433-122">Header</span></span><br/> | <dl> <span data-ttu-id="2d433-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d433-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d433-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d433-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d433-125">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="2d433-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="2d433-126">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="2d433-126">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
