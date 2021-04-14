---
description: Initialise une couleur avec les valeurs d’alpha, de rouge, de vert et de bleu fournies.
ms.assetid: e862ba1b-fdcf-4058-8835-e58b4fc5e21a
title: Macro D3DCOLOR_ARGB (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_ARGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: bd0138c435c15c0c2ac026487471554e0edf0afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322746"
---
# <a name="d3dcolor_argb-macro"></a><span data-ttu-id="35913-103">D3DCOLOR, \_ macro</span><span class="sxs-lookup"><span data-stu-id="35913-103">D3DCOLOR\_ARGB macro</span></span>

<span data-ttu-id="35913-104">Initialise une couleur avec les valeurs d’alpha, de rouge, de vert et de bleu fournies.</span><span class="sxs-lookup"><span data-stu-id="35913-104">Initializes a color with the supplied alpha, red, green, and blue values.</span></span>

## <a name="syntax"></a><span data-ttu-id="35913-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35913-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_ARGB(
   int a,
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a><span data-ttu-id="35913-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35913-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35913-107">*un*</span><span class="sxs-lookup"><span data-stu-id="35913-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="35913-108">Composant alpha de la couleur.</span><span class="sxs-lookup"><span data-stu-id="35913-108">Alpha component of the color.</span></span> <span data-ttu-id="35913-109">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="35913-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="35913-110">*r*</span><span class="sxs-lookup"><span data-stu-id="35913-110">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="35913-111">Composant rouge de la couleur.</span><span class="sxs-lookup"><span data-stu-id="35913-111">Red component of the color.</span></span> <span data-ttu-id="35913-112">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="35913-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="35913-113">*activée*</span><span class="sxs-lookup"><span data-stu-id="35913-113">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="35913-114">Composant vert de la couleur.</span><span class="sxs-lookup"><span data-stu-id="35913-114">Green component of the color.</span></span> <span data-ttu-id="35913-115">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="35913-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="35913-116">*b*</span><span class="sxs-lookup"><span data-stu-id="35913-116">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="35913-117">Composant bleu de la couleur.</span><span class="sxs-lookup"><span data-stu-id="35913-117">Blue component of the color.</span></span> <span data-ttu-id="35913-118">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="35913-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35913-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35913-119">Return value</span></span>

<span data-ttu-id="35913-120">Retourne la valeur [D3DCOLOR](d3dcolor.md) qui correspond aux valeurs ARVB fournies.</span><span class="sxs-lookup"><span data-stu-id="35913-120">Returns the [D3DCOLOR](d3dcolor.md) value that corresponds to the supplied ARGB values.</span></span>

## <a name="requirements"></a><span data-ttu-id="35913-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35913-121">Requirements</span></span>



| <span data-ttu-id="35913-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35913-122">Requirement</span></span> | <span data-ttu-id="35913-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="35913-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35913-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="35913-124">Header</span></span><br/> | <dl> <span data-ttu-id="35913-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="35913-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35913-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35913-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35913-127">Macros</span><span class="sxs-lookup"><span data-stu-id="35913-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="35913-128">**D3DCOLOR \_ RVBA**</span><span class="sxs-lookup"><span data-stu-id="35913-128">**D3DCOLOR\_RGBA**</span></span>](d3dcolor-rgba.md)
</dt> <dt>

[<span data-ttu-id="35913-129">**D3DCOLOR \_ XRGB**</span><span class="sxs-lookup"><span data-stu-id="35913-129">**D3DCOLOR\_XRGB**</span></span>](d3dcolor-xrgb.md)
</dt> </dl>

 

 




