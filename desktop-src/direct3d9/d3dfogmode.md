---
description: Définit des constantes qui décrivent le mode de brouillard.
ms.assetid: cd83c914-bc1d-4f66-b5a6-7984b7ec52cd
title: Énumération D3DFOGMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFOGMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8436a52edbb9460c6945c1526513629939ec444b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323073"
---
# <a name="d3dfogmode-enumeration"></a><span data-ttu-id="a3aab-103">Énumération D3DFOGMODE</span><span class="sxs-lookup"><span data-stu-id="a3aab-103">D3DFOGMODE enumeration</span></span>

<span data-ttu-id="a3aab-104">Définit des constantes qui décrivent le mode de brouillard.</span><span class="sxs-lookup"><span data-stu-id="a3aab-104">Defines constants that describe the fog mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3aab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3aab-105">Syntax</span></span>


```C++
typedef enum D3DFOGMODE { 
  D3DFOG_NONE         = 0,
  D3DFOG_EXP          = 1,
  D3DFOG_EXP2         = 2,
  D3DFOG_LINEAR       = 3,
  D3DFOG_FORCE_DWORD  = 0x7fffffff
} D3DFOGMODE, *LPD3DFOGMODE;
```



## <a name="constants"></a><span data-ttu-id="a3aab-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="a3aab-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a3aab-107"><span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="a3aab-107"><span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="a3aab-108">Aucun effet de brouillard.</span><span class="sxs-lookup"><span data-stu-id="a3aab-108">No fog effect.</span></span>

</dd> <dt>

<span data-ttu-id="a3aab-109"><span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG \_ exp**</span><span class="sxs-lookup"><span data-stu-id="a3aab-109"><span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG\_EXP**</span></span>
</dt> <dd>

<span data-ttu-id="a3aab-110">L’effet de brouillard augmente de façon exponentielle, en fonction de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="a3aab-110">Fog effect intensifies exponentially, according to the following formula.</span></span>

![formule d’intensité de l’effet de brouillard](images/fogexp.png)

</dd> <dt>

<span data-ttu-id="a3aab-112"><span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG \_ EXP2**</span><span class="sxs-lookup"><span data-stu-id="a3aab-112"><span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG\_EXP2**</span></span>
</dt> <dd>

<span data-ttu-id="a3aab-113">L’effet de brouillard augmente de façon exponentielle avec le carré de la distance, en fonction de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="a3aab-113">Fog effect intensifies exponentially with the square of the distance, according to the following formula.</span></span>

![formule d’intensité d’effet de brouillard basée sur le carré de distance](images/fogexp2.png)

</dd> <dt>

<span data-ttu-id="a3aab-115"><span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG \_ linéaire**</span><span class="sxs-lookup"><span data-stu-id="a3aab-115"><span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="a3aab-116">L’effet de brouillard s’intensifie de manière linéaire entre les points de départ et de fin, en fonction de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="a3aab-116">Fog effect intensifies linearly between the start and end points, according to the following formula.</span></span>

![formule d’intensité d’effet de brouillard basée sur les points de départ et de fin](images/fogliner.png)

<span data-ttu-id="a3aab-118">Il s’agit du seul mode de brouillard actuellement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a3aab-118">This is the only fog mode currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="a3aab-119"><span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a3aab-119"><span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a3aab-120">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="a3aab-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a3aab-121">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a3aab-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a3aab-122">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="a3aab-122">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3aab-123">Notes</span><span class="sxs-lookup"><span data-stu-id="a3aab-123">Remarks</span></span>

<span data-ttu-id="a3aab-124">Les valeurs de ce type énuméré sont utilisées par les États de \_ rendu D3DRS FOGTABLEMODE et D3DRS \_ FOGVERTEXMODE.</span><span class="sxs-lookup"><span data-stu-id="a3aab-124">The values in this enumerated type are used by the D3DRS\_FOGTABLEMODE and D3DRS\_FOGVERTEXMODE render states.</span></span>

<span data-ttu-id="a3aab-125">Le brouillard peut être considéré comme une mesure de visibilité : plus la valeur de brouillard produite par une équation de brouillard est faible, moins un objet est visible.</span><span class="sxs-lookup"><span data-stu-id="a3aab-125">Fog can be considered a measure of visibility: the lower the fog value produced by a fog equation, the less visible an object is.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3aab-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3aab-126">Requirements</span></span>



| <span data-ttu-id="a3aab-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3aab-127">Requirement</span></span> | <span data-ttu-id="a3aab-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3aab-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3aab-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3aab-129">Header</span></span><br/> | <dl> <span data-ttu-id="a3aab-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3aab-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3aab-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3aab-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3aab-132">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="a3aab-132">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="a3aab-133">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="a3aab-133">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
