---
description: Initialise une couleur à l’aide des valeurs (a, y, u, v).
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: Macro D3DCOLOR_AYUV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_AYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 62a34e94fbdc6c47ed034a46bdae6e9b32a7c95d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106536241"
---
# <a name="d3dcolor_ayuv-macro"></a><span data-ttu-id="67b07-103">D3DCOLOR \_ macro AYUV</span><span class="sxs-lookup"><span data-stu-id="67b07-103">D3DCOLOR\_AYUV macro</span></span>

<span data-ttu-id="67b07-104">Initialise une couleur à l’aide des valeurs (a, y, u, v).</span><span class="sxs-lookup"><span data-stu-id="67b07-104">Initializes a color using the (a,y,u,v) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="67b07-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67b07-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_AYUV(
   int a,
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a><span data-ttu-id="67b07-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67b07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67b07-107">*un*</span><span class="sxs-lookup"><span data-stu-id="67b07-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="67b07-108">Composant alpha de la couleur.</span><span class="sxs-lookup"><span data-stu-id="67b07-108">Alpha component of the color.</span></span> <span data-ttu-id="67b07-109">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="67b07-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="67b07-110">*y*</span><span class="sxs-lookup"><span data-stu-id="67b07-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="67b07-111">Composant luminance de la couleur.</span><span class="sxs-lookup"><span data-stu-id="67b07-111">Luminance component of the color.</span></span> <span data-ttu-id="67b07-112">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="67b07-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="67b07-113">*u*</span><span class="sxs-lookup"><span data-stu-id="67b07-113">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="67b07-114">Luminosité bleue de la couleur.</span><span class="sxs-lookup"><span data-stu-id="67b07-114">Blue brightness of the color.</span></span> <span data-ttu-id="67b07-115">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="67b07-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="67b07-116">*v*</span><span class="sxs-lookup"><span data-stu-id="67b07-116">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="67b07-117">Luminosité rouge de la couleur.</span><span class="sxs-lookup"><span data-stu-id="67b07-117">Red brightness of the color.</span></span> <span data-ttu-id="67b07-118">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="67b07-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67b07-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="67b07-119">Return value</span></span>

<span data-ttu-id="67b07-120">Retourne la valeur [D3DCOLOR](d3dcolor.md) qui correspond aux valeurs ARVB fournies.</span><span class="sxs-lookup"><span data-stu-id="67b07-120">Returns the [D3DCOLOR](d3dcolor.md) value that corresponds to the supplied ARGB values.</span></span>

## <a name="remarks"></a><span data-ttu-id="67b07-121">Notes</span><span class="sxs-lookup"><span data-stu-id="67b07-121">Remarks</span></span>

<span data-ttu-id="67b07-122">Une couleur RVB peut être réduite à 16 bits par pixel par conversion en luminance et les différences de couleur avec les équations suivantes :</span><span class="sxs-lookup"><span data-stu-id="67b07-122">An RGB color can be reduced to 16 bits per pixel by conversion to luminance and color differences with the following equations:</span></span>


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a><span data-ttu-id="67b07-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67b07-123">Requirements</span></span>



| <span data-ttu-id="67b07-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67b07-124">Requirement</span></span> | <span data-ttu-id="67b07-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="67b07-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67b07-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="67b07-126">Header</span></span><br/> | <dl> <span data-ttu-id="67b07-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="67b07-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67b07-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67b07-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67b07-129">Macros</span><span class="sxs-lookup"><span data-stu-id="67b07-129">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="67b07-130">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="67b07-130">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="67b07-131">**D3DCOLOR \_ XYUV**</span><span class="sxs-lookup"><span data-stu-id="67b07-131">**D3DCOLOR\_XYUV**</span></span>](d3dcolor-xyuv.md)
</dt> </dl>

 

 




