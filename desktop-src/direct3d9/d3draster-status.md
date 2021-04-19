---
description: Décrit l’état de la trame.
ms.assetid: f7b5b714-8fc8-47b8-adec-1089b8d07081
title: Structure D3DRASTER_STATUS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRASTER_STATUS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e77ab0e6ee164eadae862ed03df5652c21ba7040
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527735"
---
# <a name="d3draster_status-structure"></a><span data-ttu-id="fd975-103">\_Structure d’État D3DRASTER</span><span class="sxs-lookup"><span data-stu-id="fd975-103">D3DRASTER\_STATUS structure</span></span>

<span data-ttu-id="fd975-104">Décrit l’état de la trame.</span><span class="sxs-lookup"><span data-stu-id="fd975-104">Describes the raster status.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd975-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd975-105">Syntax</span></span>


```C++
typedef struct D3DRASTER_STATUS {
  BOOL InVBlank;
  UINT ScanLine;
} D3DRASTER_STATUS, *LPD3DRASTER_STATUS;
```



## <a name="members"></a><span data-ttu-id="fd975-106">Membres</span><span class="sxs-lookup"><span data-stu-id="fd975-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fd975-107">**InVBlank**</span><span class="sxs-lookup"><span data-stu-id="fd975-107">**InVBlank**</span></span>
</dt> <dd>

<span data-ttu-id="fd975-108">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd975-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fd975-109">**True** si le raster est dans la période vide verticale.</span><span class="sxs-lookup"><span data-stu-id="fd975-109">**TRUE** if the raster is in the vertical blank period.</span></span> <span data-ttu-id="fd975-110">**False** si le raster n’est pas dans la période vide verticale.</span><span class="sxs-lookup"><span data-stu-id="fd975-110">**FALSE** if the raster is not in the vertical blank period.</span></span>

</dd> <dt>

<span data-ttu-id="fd975-111">**Numérisation**</span><span class="sxs-lookup"><span data-stu-id="fd975-111">**ScanLine**</span></span>
</dt> <dd>

<span data-ttu-id="fd975-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd975-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fd975-113">Si InVBlank a la valeur **false**, cette valeur est un entier qui correspond approximativement à la ligne de numérisation actuelle peinte par le raster.</span><span class="sxs-lookup"><span data-stu-id="fd975-113">If InVBlank is **FALSE**, then this value is an integer roughly corresponding to the current scan line painted by the raster.</span></span> <span data-ttu-id="fd975-114">Les lignes de numérisation sont numérotées de la même façon que les coordonnées de la surface Direct3D : 0 est le haut de la surface primaire, qui s’étend jusqu’à la valeur (hauteur de la surface-1) en bas de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="fd975-114">Scan lines are numbered in the same way as Direct3D surface coordinates: 0 is the top of the primary surface, extending to the value (height of the surface - 1) at the bottom of the display.</span></span>

<span data-ttu-id="fd975-115">Si InVBlank a la valeur **true**, cette valeur est définie à zéro et peut être ignorée.</span><span class="sxs-lookup"><span data-stu-id="fd975-115">If InVBlank is **TRUE**, then this value is set to zero and can be ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd975-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd975-116">Requirements</span></span>



| <span data-ttu-id="fd975-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd975-117">Requirement</span></span> | <span data-ttu-id="fd975-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd975-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd975-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd975-119">Header</span></span><br/> | <dl> <span data-ttu-id="fd975-120"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd975-120"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd975-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd975-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd975-122">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="fd975-122">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="fd975-123">**GetRasterStatus**</span><span class="sxs-lookup"><span data-stu-id="fd975-123">**GetRasterStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
