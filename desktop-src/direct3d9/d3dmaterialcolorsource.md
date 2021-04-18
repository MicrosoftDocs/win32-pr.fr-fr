---
description: Définit l’emplacement auquel un composant couleur ou couleur doit être accédé pour les calculs d’éclairage.
ms.assetid: 76061d47-a31c-4008-aa8d-a0464dd3423f
title: Énumération D3DMATERIALCOLORSOURCE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIALCOLORSOURCE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8877eece8e33c6508768b22c989e992cf8178823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543028"
---
# <a name="d3dmaterialcolorsource-enumeration"></a><span data-ttu-id="7032e-103">Énumération D3DMATERIALCOLORSOURCE</span><span class="sxs-lookup"><span data-stu-id="7032e-103">D3DMATERIALCOLORSOURCE enumeration</span></span>

<span data-ttu-id="7032e-104">Définit l’emplacement auquel un composant couleur ou couleur doit être accédé pour les calculs d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="7032e-104">Defines the location at which a color or color component must be accessed for lighting calculations.</span></span>

## <a name="syntax"></a><span data-ttu-id="7032e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7032e-105">Syntax</span></span>


```C++
typedef enum D3DMATERIALCOLORSOURCE { 
  D3DMCS_MATERIAL     = 0,
  D3DMCS_COLOR1       = 1,
  D3DMCS_COLOR2       = 2,
  D3DMCS_FORCE_DWORD  = 0x7fffffff
} D3DMATERIALCOLORSOURCE, *LPD3DMATERIALCOLORSOURCE;
```



## <a name="constants"></a><span data-ttu-id="7032e-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="7032e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7032e-107"><span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**\_Matériau D3DMCS**</span><span class="sxs-lookup"><span data-stu-id="7032e-107"><span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**D3DMCS\_MATERIAL**</span></span>
</dt> <dd>

<span data-ttu-id="7032e-108">Utilisez la couleur de la matière actuelle.</span><span class="sxs-lookup"><span data-stu-id="7032e-108">Use the color from the current material.</span></span>

</dd> <dt>

<span data-ttu-id="7032e-109"><span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS \_ COLOR1**</span><span class="sxs-lookup"><span data-stu-id="7032e-109"><span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS\_COLOR1**</span></span>
</dt> <dd>

<span data-ttu-id="7032e-110">Utilisez la couleur de vertex diffuse.</span><span class="sxs-lookup"><span data-stu-id="7032e-110">Use the diffuse vertex color.</span></span>

</dd> <dt>

<span data-ttu-id="7032e-111"><span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS \_ COLOR2**</span><span class="sxs-lookup"><span data-stu-id="7032e-111"><span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS\_COLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="7032e-112">Utilisez la couleur de vertex spéculaire.</span><span class="sxs-lookup"><span data-stu-id="7032e-112">Use the specular vertex color.</span></span>

</dd> <dt>

<span data-ttu-id="7032e-113"><span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="7032e-113"><span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="7032e-114">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="7032e-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="7032e-115">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7032e-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="7032e-116">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="7032e-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7032e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="7032e-117">Remarks</span></span>

<span data-ttu-id="7032e-118">Ces indicateurs sont utilisés pour définir la valeur des États de rendu suivants dans le type énuméré [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) .</span><span class="sxs-lookup"><span data-stu-id="7032e-118">These flags are used to set the value of the following render states in the [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type.</span></span>

-   <span data-ttu-id="7032e-119">D3DRS \_ AMBIENTMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="7032e-119">D3DRS\_AMBIENTMATERIALSOURCE</span></span>
-   <span data-ttu-id="7032e-120">D3DRS \_ DIFFUSEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="7032e-120">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>
-   <span data-ttu-id="7032e-121">D3DRS \_ EMISSIVEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="7032e-121">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>
-   <span data-ttu-id="7032e-122">D3DRS \_ SPECULARMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="7032e-122">D3DRS\_SPECULARMATERIALSOURCE</span></span>

## <a name="requirements"></a><span data-ttu-id="7032e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7032e-123">Requirements</span></span>



| <span data-ttu-id="7032e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7032e-124">Requirement</span></span> | <span data-ttu-id="7032e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="7032e-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7032e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="7032e-126">Header</span></span><br/> | <dl> <span data-ttu-id="7032e-127"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7032e-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7032e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7032e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7032e-129">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="7032e-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="7032e-130">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="7032e-130">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
