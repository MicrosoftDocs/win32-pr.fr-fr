---
description: Initialise une couleur avec les valeurs de rouge, vert et bleu fournies.
ms.assetid: 832a4a78-c166-4e45-a907-57730da1c2c8
title: Macro D3DCOLOR_XRGB (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XRGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 4932e34979b0913f27874e57cfa881f18fb16364
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394080"
---
# <a name="d3dcolor_xrgb-macro"></a><span data-ttu-id="a1c0a-103">D3DCOLOR \_ macro XRGB</span><span class="sxs-lookup"><span data-stu-id="a1c0a-103">D3DCOLOR\_XRGB macro</span></span>

<span data-ttu-id="a1c0a-104">Initialise une couleur avec les valeurs de rouge, vert et bleu fournies.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-104">Initializes a color with the supplied red, green, and blue values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1c0a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1c0a-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_XRGB(
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a><span data-ttu-id="a1c0a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1c0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1c0a-107">*r*</span><span class="sxs-lookup"><span data-stu-id="a1c0a-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="a1c0a-108">Composant rouge de la couleur.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-108">Red component of the color.</span></span> <span data-ttu-id="a1c0a-109">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="a1c0a-110">*activée*</span><span class="sxs-lookup"><span data-stu-id="a1c0a-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="a1c0a-111">Composant vert de la couleur.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-111">Green component of the color.</span></span> <span data-ttu-id="a1c0a-112">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="a1c0a-113">*b*</span><span class="sxs-lookup"><span data-stu-id="a1c0a-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="a1c0a-114">Composant bleu de la couleur.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-114">Blue component of the color.</span></span> <span data-ttu-id="a1c0a-115">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-115">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1c0a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a1c0a-116">Return value</span></span>

<span data-ttu-id="a1c0a-117">Retourne la valeur [**D3DCOLOR**](d3dcolor.md) qui correspond aux valeurs RVB fournies.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-117">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGB values.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1c0a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1c0a-118">Requirements</span></span>



| <span data-ttu-id="a1c0a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1c0a-119">Requirement</span></span> | <span data-ttu-id="a1c0a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1c0a-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1c0a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1c0a-121">Header</span></span><br/> | <dl> <span data-ttu-id="a1c0a-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1c0a-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1c0a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1c0a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1c0a-124">Macros</span><span class="sxs-lookup"><span data-stu-id="a1c0a-124">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="a1c0a-125">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="a1c0a-125">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="a1c0a-126">**D3DCOLOR \_ RVBA**</span><span class="sxs-lookup"><span data-stu-id="a1c0a-126">**D3DCOLOR\_RGBA**</span></span>](d3dcolor-rgba.md)
</dt> </dl>

 

 




