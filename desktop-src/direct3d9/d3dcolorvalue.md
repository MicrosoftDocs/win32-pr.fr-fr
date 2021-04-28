---
description: D3DCOLORVALUE structure (D3D9Types. h)-décrit les valeurs de couleur.
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: D3DCOLORVALUE, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: c9b55fbf718382e9dca7e3999cce0cabe895a261
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116057"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a><span data-ttu-id="6310d-103">D3DCOLORVALUE, structure (D3D9Types. h)</span><span class="sxs-lookup"><span data-stu-id="6310d-103">D3DCOLORVALUE structure (D3D9Types.h)</span></span>

<span data-ttu-id="6310d-104">Décrit les valeurs de couleur.</span><span class="sxs-lookup"><span data-stu-id="6310d-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="6310d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6310d-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="6310d-106">Membres</span><span class="sxs-lookup"><span data-stu-id="6310d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6310d-107">**r**</span><span class="sxs-lookup"><span data-stu-id="6310d-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="6310d-108">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="6310d-108">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="6310d-109">Valeur à virgule flottante qui spécifie le composant rouge d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="6310d-109">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="6310d-110">Cette valeur est généralement comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="6310d-110">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="6310d-111">La valeur 0,0 indique l’absence totale du composant rouge, tandis que la valeur 1,0 indique que le rouge est entièrement présent.</span><span class="sxs-lookup"><span data-stu-id="6310d-111">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="6310d-112">**activée**</span><span class="sxs-lookup"><span data-stu-id="6310d-112">**g**</span></span>
</dt> <dd>

<span data-ttu-id="6310d-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="6310d-113">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="6310d-114">Valeur à virgule flottante qui spécifie le composant vert d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="6310d-114">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="6310d-115">Cette valeur est généralement comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="6310d-115">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="6310d-116">La valeur 0,0 indique l’absence totale du composant vert, tandis que la valeur 1,0 indique que le vert est entièrement présent.</span><span class="sxs-lookup"><span data-stu-id="6310d-116">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="6310d-117">**b**</span><span class="sxs-lookup"><span data-stu-id="6310d-117">**b**</span></span>
</dt> <dd>

<span data-ttu-id="6310d-118">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="6310d-118">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="6310d-119">Valeur à virgule flottante qui spécifie le composant bleu d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="6310d-119">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="6310d-120">Cette valeur est généralement comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="6310d-120">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="6310d-121">La valeur 0,0 indique l’absence totale du composant bleu, tandis que la valeur 1,0 indique que le bleu est entièrement présent.</span><span class="sxs-lookup"><span data-stu-id="6310d-121">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="6310d-122">**un**</span><span class="sxs-lookup"><span data-stu-id="6310d-122">**a**</span></span>
</dt> <dd>

<span data-ttu-id="6310d-123">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="6310d-123">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="6310d-124">Valeur à virgule flottante qui spécifie le composant alpha d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="6310d-124">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="6310d-125">Cette valeur est généralement comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="6310d-125">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="6310d-126">Une valeur de 0,0 indique une transparence complète, tandis que la valeur 1,0 indique une opacité totale.</span><span class="sxs-lookup"><span data-stu-id="6310d-126">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6310d-127">Notes </span><span class="sxs-lookup"><span data-stu-id="6310d-127">Remarks</span></span>

<span data-ttu-id="6310d-128">Vous pouvez définir les membres de cette structure sur des valeurs situées en dehors de la plage comprise entre 0 et 1 pour implémenter des effets inhabituels.</span><span class="sxs-lookup"><span data-stu-id="6310d-128">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="6310d-129">Les valeurs supérieures à 1 produisent des lumières fortes qui ont tendance à nettoyer une scène.</span><span class="sxs-lookup"><span data-stu-id="6310d-129">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="6310d-130">Les valeurs négatives produisent des lumières sombres qui suppriment en fait la lumière d’une scène.</span><span class="sxs-lookup"><span data-stu-id="6310d-130">Negative values produce dark lights that actually remove light from a scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="6310d-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6310d-131">Requirements</span></span>



| <span data-ttu-id="6310d-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6310d-132">Requirement</span></span> | <span data-ttu-id="6310d-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="6310d-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6310d-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="6310d-134">Header</span></span><br/> | <dl> <span data-ttu-id="6310d-135"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6310d-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6310d-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6310d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6310d-137">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="6310d-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




