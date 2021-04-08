---
description: Représente une valeur de couleur avec alpha, qui est utilisé pour la transparence.
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: Structure DXGI_RGBA (DXGItype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_RGBA
api_type:
- HeaderDef
api_location:
- DXGItype.h
ms.openlocfilehash: 77b526e916d43868304c6c01a7dbbe8ebbb5692b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746765"
---
# <a name="dxgi_rgba-structure"></a><span data-ttu-id="69c77-103">DXGI \_ RVBA, structure</span><span class="sxs-lookup"><span data-stu-id="69c77-103">DXGI\_RGBA structure</span></span>

<span data-ttu-id="69c77-104">Représente une valeur de couleur avec alpha, qui est utilisé pour la transparence.</span><span class="sxs-lookup"><span data-stu-id="69c77-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="69c77-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69c77-105">Syntax</span></span>


```C++
typedef struct _DXGI_RGBA {
  float r;
  float g;
  float b;
  float a;
} DXGI_RGBA;
```



## <a name="members"></a><span data-ttu-id="69c77-106">Membres</span><span class="sxs-lookup"><span data-stu-id="69c77-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="69c77-107">**r**</span><span class="sxs-lookup"><span data-stu-id="69c77-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="69c77-108">Valeur à virgule flottante qui spécifie le composant rouge d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="69c77-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="69c77-109">Cette valeur est généralement comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="69c77-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="69c77-110">La valeur 0,0 indique l’absence totale du composant rouge, tandis que la valeur 1,0 indique que le rouge est entièrement présent.</span><span class="sxs-lookup"><span data-stu-id="69c77-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="69c77-111">**activée**</span><span class="sxs-lookup"><span data-stu-id="69c77-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="69c77-112">Valeur à virgule flottante qui spécifie le composant vert d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="69c77-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="69c77-113">Cette valeur est généralement comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="69c77-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="69c77-114">La valeur 0,0 indique l’absence totale du composant vert, tandis que la valeur 1,0 indique que le vert est entièrement présent.</span><span class="sxs-lookup"><span data-stu-id="69c77-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="69c77-115">**b**</span><span class="sxs-lookup"><span data-stu-id="69c77-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="69c77-116">Valeur à virgule flottante qui spécifie le composant bleu d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="69c77-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="69c77-117">Cette valeur est généralement comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="69c77-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="69c77-118">La valeur 0,0 indique l’absence totale du composant bleu, tandis que la valeur 1,0 indique que le bleu est entièrement présent.</span><span class="sxs-lookup"><span data-stu-id="69c77-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="69c77-119">**un**</span><span class="sxs-lookup"><span data-stu-id="69c77-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="69c77-120">Valeur à virgule flottante qui spécifie le composant alpha d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="69c77-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="69c77-121">Cette valeur est généralement comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="69c77-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="69c77-122">Une valeur de 0,0 indique une transparence complète, tandis que la valeur 1,0 indique une opacité totale.</span><span class="sxs-lookup"><span data-stu-id="69c77-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69c77-123">Notes</span><span class="sxs-lookup"><span data-stu-id="69c77-123">Remarks</span></span>

<span data-ttu-id="69c77-124">Vous pouvez définir les membres de cette structure sur des valeurs situées en dehors de la plage comprise entre 0 et 1 pour implémenter des effets inhabituels.</span><span class="sxs-lookup"><span data-stu-id="69c77-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="69c77-125">Les valeurs supérieures à 1 produisent des lumières fortes qui ont tendance à nettoyer une scène.</span><span class="sxs-lookup"><span data-stu-id="69c77-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="69c77-126">Les valeurs négatives produisent des lumières sombres qui suppriment en fait la lumière d’une scène.</span><span class="sxs-lookup"><span data-stu-id="69c77-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="69c77-127">Le type d’en-tête DXGItype. h-définit **dxgi \_ RVBA** comme un alias de [**D3DCOLORVALUE**](d3dcolorvalue.md), comme suit :</span><span class="sxs-lookup"><span data-stu-id="69c77-127">The DXGItype.h header type-defines **DXGI\_RGBA** as an alias of [**D3DCOLORVALUE**](d3dcolorvalue.md), as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="69c77-128">Vous pouvez utiliser **dxgi \_ RVBA** avec [**IDXGISwapChain1 :: SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1 :: GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)et le [**\_ \_ mode Alpha dxgi**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span><span class="sxs-lookup"><span data-stu-id="69c77-128">You can use **DXGI\_RGBA** with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="69c77-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69c77-129">Requirements</span></span>



| <span data-ttu-id="69c77-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69c77-130">Requirement</span></span> | <span data-ttu-id="69c77-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="69c77-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69c77-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69c77-132">Minimum supported client</span></span><br/> | <span data-ttu-id="69c77-133">Windows 8 et mise à jour de plateforme pour les applications de \[ Bureau UWP Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="69c77-133">Windows 8 and Platform Update for Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="69c77-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69c77-134">Minimum supported server</span></span><br/> | <span data-ttu-id="69c77-135">Windows Server 2012 et la mise à jour de la plateforme pour les applications de bureau Windows Server 2008 R2 pour les applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="69c77-135">Windows Server 2012 and Platform Update for Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="69c77-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="69c77-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="69c77-137"><dt>DXGItype. h</dt></span><span class="sxs-lookup"><span data-stu-id="69c77-137"><dt>DXGItype.h</dt></span></span> </dl>                      |



## <a name="see-also"></a><span data-ttu-id="69c77-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69c77-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69c77-139">Structures DXGI</span><span class="sxs-lookup"><span data-stu-id="69c77-139">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="69c77-140">**D3DCOLORVALUE**</span><span class="sxs-lookup"><span data-stu-id="69c77-140">**D3DCOLORVALUE**</span></span>](d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="69c77-141">**D3DCOLORVALUE (dans Direct3D 9)**</span><span class="sxs-lookup"><span data-stu-id="69c77-141">**D3DCOLORVALUE (in Direct3D 9)**</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
