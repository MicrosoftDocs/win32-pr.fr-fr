---
description: Initialise une couleur avec les valeurs (y, u, v).
ms.assetid: e3091eaf-8639-428c-8dd8-6feeb7d7776e
title: Macro D3DCOLOR_XYUV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 12d539e44528c5e54a54209763e4cbe262cd16f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870086"
---
# <a name="d3dcolor_xyuv-macro"></a><span data-ttu-id="2006a-103">D3DCOLOR \_ macro XYUV</span><span class="sxs-lookup"><span data-stu-id="2006a-103">D3DCOLOR\_XYUV macro</span></span>

<span data-ttu-id="2006a-104">Initialise une couleur avec les valeurs (y, u, v).</span><span class="sxs-lookup"><span data-stu-id="2006a-104">Initializes a color with the (y, u, v) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="2006a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2006a-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_XYUV(
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a><span data-ttu-id="2006a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2006a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2006a-107">*y*</span><span class="sxs-lookup"><span data-stu-id="2006a-107">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="2006a-108">Composant luminance de la couleur.</span><span class="sxs-lookup"><span data-stu-id="2006a-108">Luminance component of the color.</span></span> <span data-ttu-id="2006a-109">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="2006a-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="2006a-110">*u*</span><span class="sxs-lookup"><span data-stu-id="2006a-110">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="2006a-111">Luminosité bleue de la couleur.</span><span class="sxs-lookup"><span data-stu-id="2006a-111">Blue brightness of the color.</span></span> <span data-ttu-id="2006a-112">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="2006a-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="2006a-113">*v*</span><span class="sxs-lookup"><span data-stu-id="2006a-113">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="2006a-114">Luminosité rouge de la couleur.</span><span class="sxs-lookup"><span data-stu-id="2006a-114">Red brightness of the color.</span></span> <span data-ttu-id="2006a-115">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="2006a-115">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2006a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2006a-116">Return value</span></span>

<span data-ttu-id="2006a-117">Retourne la valeur [**D3DCOLOR**](d3dcolor.md) qui correspond aux valeurs fournies (y, u, v).</span><span class="sxs-lookup"><span data-stu-id="2006a-117">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied (y, u, v) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="2006a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="2006a-118">Remarks</span></span>

<span data-ttu-id="2006a-119">Une couleur RVB peut être réduite à 16 bits par pixel par conversion en luminance et les différences de couleur avec les équations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2006a-119">An RGB color can be reduced to 16 bits per pixel by conversion to luminance and color differences with the following equations:</span></span>


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a><span data-ttu-id="2006a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2006a-120">Requirements</span></span>



| <span data-ttu-id="2006a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2006a-121">Requirement</span></span> | <span data-ttu-id="2006a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="2006a-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2006a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="2006a-123">Header</span></span><br/> | <dl> <span data-ttu-id="2006a-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2006a-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2006a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2006a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2006a-126">Macros</span><span class="sxs-lookup"><span data-stu-id="2006a-126">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="2006a-127">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="2006a-127">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="2006a-128">**D3DCOLOR \_ AYUV**</span><span class="sxs-lookup"><span data-stu-id="2006a-128">**D3DCOLOR\_AYUV**</span></span>](d3dcolor-ayuv.md)
</dt> </dl>

 

 




