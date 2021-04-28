---
description: 'D3DCOLORVALUE structure (Dxgitype. h) : représente une valeur de couleur avec alpha, qui est utilisée pour la transparence.'
ms.assetid: 27A86A10-FC0E-421E-BEA7-2DEB539849BB
title: D3DCOLORVALUE, structure (Dxgitype. h)
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
- dxgitype.h
ms.openlocfilehash: 83ca500493a04f04de5352185c240d20a19009f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107147"
---
# <a name="d3dcolorvalue-structure-dxgitypeh"></a><span data-ttu-id="24e6a-103">D3DCOLORVALUE, structure (Dxgitype. h)</span><span class="sxs-lookup"><span data-stu-id="24e6a-103">D3DCOLORVALUE structure (Dxgitype.h)</span></span>

<span data-ttu-id="24e6a-104">Représente une valeur de couleur avec alpha, qui est utilisé pour la transparence.</span><span class="sxs-lookup"><span data-stu-id="24e6a-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="24e6a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24e6a-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="24e6a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="24e6a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="24e6a-107">**r**</span><span class="sxs-lookup"><span data-stu-id="24e6a-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="24e6a-108">Valeur à virgule flottante qui spécifie le composant rouge d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="24e6a-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="24e6a-109">Cette valeur est généralement comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="24e6a-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="24e6a-110">La valeur 0,0 indique l’absence totale du composant rouge, tandis que la valeur 1,0 indique que le rouge est entièrement présent.</span><span class="sxs-lookup"><span data-stu-id="24e6a-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="24e6a-111">**activée**</span><span class="sxs-lookup"><span data-stu-id="24e6a-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="24e6a-112">Valeur à virgule flottante qui spécifie le composant vert d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="24e6a-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="24e6a-113">Cette valeur est généralement comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="24e6a-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="24e6a-114">La valeur 0,0 indique l’absence totale du composant vert, tandis que la valeur 1,0 indique que le vert est entièrement présent.</span><span class="sxs-lookup"><span data-stu-id="24e6a-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="24e6a-115">**b**</span><span class="sxs-lookup"><span data-stu-id="24e6a-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="24e6a-116">Valeur à virgule flottante qui spécifie le composant bleu d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="24e6a-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="24e6a-117">Cette valeur est généralement comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="24e6a-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="24e6a-118">La valeur 0,0 indique l’absence totale du composant bleu, tandis que la valeur 1,0 indique que le bleu est entièrement présent.</span><span class="sxs-lookup"><span data-stu-id="24e6a-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="24e6a-119">**un**</span><span class="sxs-lookup"><span data-stu-id="24e6a-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="24e6a-120">Valeur à virgule flottante qui spécifie le composant alpha d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="24e6a-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="24e6a-121">Cette valeur est généralement comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="24e6a-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="24e6a-122">Une valeur de 0,0 indique une transparence complète, tandis que la valeur 1,0 indique une opacité totale.</span><span class="sxs-lookup"><span data-stu-id="24e6a-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24e6a-123">Notes </span><span class="sxs-lookup"><span data-stu-id="24e6a-123">Remarks</span></span>

<span data-ttu-id="24e6a-124">Vous pouvez définir les membres de cette structure sur des valeurs situées en dehors de la plage comprise entre 0 et 1 pour implémenter des effets inhabituels.</span><span class="sxs-lookup"><span data-stu-id="24e6a-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="24e6a-125">Les valeurs supérieures à 1 produisent des lumières fortes qui ont tendance à nettoyer une scène.</span><span class="sxs-lookup"><span data-stu-id="24e6a-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="24e6a-126">Les valeurs négatives produisent des lumières sombres qui suppriment en fait la lumière d’une scène.</span><span class="sxs-lookup"><span data-stu-id="24e6a-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="24e6a-127">Le type d’en-tête DXGItype. h-définit [**dxgi \_ RVBA**](dxgi-rgba.md) comme un alias de **D3DCOLORVALUE**, comme suit :</span><span class="sxs-lookup"><span data-stu-id="24e6a-127">The DXGItype.h header type-defines [**DXGI\_RGBA**](dxgi-rgba.md) as an alias of **D3DCOLORVALUE**, as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="24e6a-128">Vous pouvez utiliser D3DCOLORVALUE ou [**dxgi \_ RVBA**](dxgi-rgba.md) avec [**IDXGISwapChain1 :: SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1 :: GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)et le [**\_ \_ mode Alpha dxgi**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span><span class="sxs-lookup"><span data-stu-id="24e6a-128">You can use D3DCOLORVALUE or [**DXGI\_RGBA**](dxgi-rgba.md) with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="24e6a-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24e6a-129">Requirements</span></span>



| <span data-ttu-id="24e6a-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24e6a-130">Requirement</span></span> | <span data-ttu-id="24e6a-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="24e6a-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24e6a-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="24e6a-132">Header</span></span><br/> | <dl> <span data-ttu-id="24e6a-133"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="24e6a-133"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24e6a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24e6a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24e6a-135">Structures DXGI</span><span class="sxs-lookup"><span data-stu-id="24e6a-135">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="24e6a-136">**DXGI \_ RVBA**</span><span class="sxs-lookup"><span data-stu-id="24e6a-136">**DXGI\_RGBA**</span></span>](dxgi-rgba.md)
</dt> </dl>

 

 




