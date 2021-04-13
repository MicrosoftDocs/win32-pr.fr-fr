---
description: Représente une valeur de couleur avec alpha, qui est utilisé pour la transparence.
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
ms.openlocfilehash: 2b7d768af9e471f3183c6a400622c2b0e0719a2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322881"
---
# <a name="d3dcolorvalue-structure-dxgitypeh"></a><span data-ttu-id="83c4f-103">D3DCOLORVALUE, structure (Dxgitype. h)</span><span class="sxs-lookup"><span data-stu-id="83c4f-103">D3DCOLORVALUE structure (Dxgitype.h)</span></span>

<span data-ttu-id="83c4f-104">Représente une valeur de couleur avec alpha, qui est utilisé pour la transparence.</span><span class="sxs-lookup"><span data-stu-id="83c4f-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="83c4f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83c4f-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="83c4f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="83c4f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="83c4f-107">**r**</span><span class="sxs-lookup"><span data-stu-id="83c4f-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="83c4f-108">Valeur à virgule flottante qui spécifie le composant rouge d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="83c4f-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="83c4f-109">Cette valeur est généralement comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="83c4f-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="83c4f-110">La valeur 0,0 indique l’absence totale du composant rouge, tandis que la valeur 1,0 indique que le rouge est entièrement présent.</span><span class="sxs-lookup"><span data-stu-id="83c4f-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="83c4f-111">**activée**</span><span class="sxs-lookup"><span data-stu-id="83c4f-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="83c4f-112">Valeur à virgule flottante qui spécifie le composant vert d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="83c4f-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="83c4f-113">Cette valeur est généralement comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="83c4f-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="83c4f-114">La valeur 0,0 indique l’absence totale du composant vert, tandis que la valeur 1,0 indique que le vert est entièrement présent.</span><span class="sxs-lookup"><span data-stu-id="83c4f-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="83c4f-115">**b**</span><span class="sxs-lookup"><span data-stu-id="83c4f-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="83c4f-116">Valeur à virgule flottante qui spécifie le composant bleu d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="83c4f-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="83c4f-117">Cette valeur est généralement comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="83c4f-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="83c4f-118">La valeur 0,0 indique l’absence totale du composant bleu, tandis que la valeur 1,0 indique que le bleu est entièrement présent.</span><span class="sxs-lookup"><span data-stu-id="83c4f-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="83c4f-119">**un**</span><span class="sxs-lookup"><span data-stu-id="83c4f-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="83c4f-120">Valeur à virgule flottante qui spécifie le composant alpha d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="83c4f-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="83c4f-121">Cette valeur est généralement comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="83c4f-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="83c4f-122">Une valeur de 0,0 indique une transparence complète, tandis que la valeur 1,0 indique une opacité totale.</span><span class="sxs-lookup"><span data-stu-id="83c4f-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83c4f-123">Notes</span><span class="sxs-lookup"><span data-stu-id="83c4f-123">Remarks</span></span>

<span data-ttu-id="83c4f-124">Vous pouvez définir les membres de cette structure sur des valeurs situées en dehors de la plage comprise entre 0 et 1 pour implémenter des effets inhabituels.</span><span class="sxs-lookup"><span data-stu-id="83c4f-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="83c4f-125">Les valeurs supérieures à 1 produisent des lumières fortes qui ont tendance à nettoyer une scène.</span><span class="sxs-lookup"><span data-stu-id="83c4f-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="83c4f-126">Les valeurs négatives produisent des lumières sombres qui suppriment en fait la lumière d’une scène.</span><span class="sxs-lookup"><span data-stu-id="83c4f-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="83c4f-127">Le type d’en-tête DXGItype. h-définit [**dxgi \_ RVBA**](dxgi-rgba.md) comme un alias de **D3DCOLORVALUE**, comme suit :</span><span class="sxs-lookup"><span data-stu-id="83c4f-127">The DXGItype.h header type-defines [**DXGI\_RGBA**](dxgi-rgba.md) as an alias of **D3DCOLORVALUE**, as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="83c4f-128">Vous pouvez utiliser D3DCOLORVALUE ou [**dxgi \_ RVBA**](dxgi-rgba.md) avec [**IDXGISwapChain1 :: SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1 :: GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)et le [**\_ \_ mode Alpha dxgi**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span><span class="sxs-lookup"><span data-stu-id="83c4f-128">You can use D3DCOLORVALUE or [**DXGI\_RGBA**](dxgi-rgba.md) with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="83c4f-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83c4f-129">Requirements</span></span>



| <span data-ttu-id="83c4f-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83c4f-130">Requirement</span></span> | <span data-ttu-id="83c4f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="83c4f-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83c4f-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="83c4f-132">Header</span></span><br/> | <dl> <span data-ttu-id="83c4f-133"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="83c4f-133"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83c4f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83c4f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83c4f-135">Structures DXGI</span><span class="sxs-lookup"><span data-stu-id="83c4f-135">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="83c4f-136">**DXGI \_ RVBA**</span><span class="sxs-lookup"><span data-stu-id="83c4f-136">**DXGI\_RGBA**</span></span>](dxgi-rgba.md)
</dt> </dl>

 

 




