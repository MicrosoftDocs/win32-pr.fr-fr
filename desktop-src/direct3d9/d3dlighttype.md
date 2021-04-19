---
description: Définit le type de lumière.
ms.assetid: 90ad82d3-ffa8-42bb-9d9c-cf28a416c32d
title: Énumération D3DLIGHTTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHTTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 83c94db3126443f757f01a69d7d773417f70683a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542168"
---
# <a name="d3dlighttype-enumeration"></a><span data-ttu-id="cf035-103">Énumération D3DLIGHTTYPE</span><span class="sxs-lookup"><span data-stu-id="cf035-103">D3DLIGHTTYPE enumeration</span></span>

<span data-ttu-id="cf035-104">Définit le type de lumière.</span><span class="sxs-lookup"><span data-stu-id="cf035-104">Defines the light type.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf035-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf035-105">Syntax</span></span>


```C++
typedef enum D3DLIGHTTYPE { 
  D3DLIGHT_POINT        = 1,
  D3DLIGHT_SPOT         = 2,
  D3DLIGHT_DIRECTIONAL  = 3,
  D3DLIGHT_FORCE_DWORD  = 0x7fffffff
} D3DLIGHTTYPE, *LPD3DLIGHTTYPE;
```



## <a name="constants"></a><span data-ttu-id="cf035-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="cf035-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cf035-107"><span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**\_Point D3DLIGHT**</span><span class="sxs-lookup"><span data-stu-id="cf035-107"><span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**D3DLIGHT\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="cf035-108">Light est une source de point.</span><span class="sxs-lookup"><span data-stu-id="cf035-108">Light is a point source.</span></span> <span data-ttu-id="cf035-109">La lumière a une position dans l’espace et rayonne la lumière dans toutes les directions.</span><span class="sxs-lookup"><span data-stu-id="cf035-109">The light has a position in space and radiates light in all directions.</span></span>

</dd> <dt>

<span data-ttu-id="cf035-110"><span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT \_**</span><span class="sxs-lookup"><span data-stu-id="cf035-110"><span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="cf035-111">Light est une source Spotlight.</span><span class="sxs-lookup"><span data-stu-id="cf035-111">Light is a spotlight source.</span></span> <span data-ttu-id="cf035-112">Cette lumière est semblable à une lumière de point, sauf que l’éclairage est limité à un cône.</span><span class="sxs-lookup"><span data-stu-id="cf035-112">This light is like a point light, except that the illumination is limited to a cone.</span></span> <span data-ttu-id="cf035-113">Ce type de lumière a une direction et plusieurs autres paramètres qui déterminent la forme du cône qu’il produit.</span><span class="sxs-lookup"><span data-stu-id="cf035-113">This light type has a direction and several other parameters that determine the shape of the cone it produces.</span></span> <span data-ttu-id="cf035-114">Pour plus d’informations sur ces paramètres, consultez la structure [**D3DLIGHT9**](d3dlight9.md) .</span><span class="sxs-lookup"><span data-stu-id="cf035-114">For information about these parameters, see the [**D3DLIGHT9**](d3dlight9.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cf035-115"><span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT \_ directionnelle**</span><span class="sxs-lookup"><span data-stu-id="cf035-115"><span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT\_DIRECTIONAL**</span></span>
</dt> <dd>

<span data-ttu-id="cf035-116">Light est une source de lumière directionnelle.</span><span class="sxs-lookup"><span data-stu-id="cf035-116">Light is a directional light source.</span></span> <span data-ttu-id="cf035-117">Cela équivaut à utiliser une source de lumière de point à une distance infinie.</span><span class="sxs-lookup"><span data-stu-id="cf035-117">This is equivalent to using a point light source at an infinite distance.</span></span>

</dd> <dt>

<span data-ttu-id="cf035-118"><span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="cf035-118"><span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="cf035-119">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="cf035-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="cf035-120">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="cf035-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="cf035-121">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="cf035-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf035-122">Notes</span><span class="sxs-lookup"><span data-stu-id="cf035-122">Remarks</span></span>

<span data-ttu-id="cf035-123">Les lumières directionnelles sont légèrement plus rapides que les sources de point-lumière, mais les lumières de point sont un peu mieux adaptées.</span><span class="sxs-lookup"><span data-stu-id="cf035-123">Directional lights are slightly faster than point light sources, but point lights look a little better.</span></span> <span data-ttu-id="cf035-124">Les actualités offrent des effets visuels intéressants, mais prennent du temps sur le calcul.</span><span class="sxs-lookup"><span data-stu-id="cf035-124">Spotlights offer interesting visual effects but are computationally time-consuming.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf035-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf035-125">Requirements</span></span>



| <span data-ttu-id="cf035-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf035-126">Requirement</span></span> | <span data-ttu-id="cf035-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf035-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf035-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf035-128">Header</span></span><br/> | <dl> <span data-ttu-id="cf035-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf035-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf035-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf035-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf035-131">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="cf035-131">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="cf035-132">**D3DLIGHT9**</span><span class="sxs-lookup"><span data-stu-id="cf035-132">**D3DLIGHT9**</span></span>](d3dlight9.md)
</dt> </dl>

 

 




