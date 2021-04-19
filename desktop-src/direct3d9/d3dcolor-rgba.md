---
description: Initialise une couleur avec les valeurs de rouge, vert, bleu et alpha fournies.
ms.assetid: 87d322f1-4a26-42fd-a1c3-7be220cecf0f
title: Macro D3DCOLOR_RGBA (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_RGBA
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c5047f29a9afbe5bb18db213f90e559b5e11d273
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523814"
---
# <a name="d3dcolor_rgba-macro"></a><span data-ttu-id="f63c3-103">D3DCOLOR, \_ macro</span><span class="sxs-lookup"><span data-stu-id="f63c3-103">D3DCOLOR\_RGBA macro</span></span>

<span data-ttu-id="f63c3-104">Initialise une couleur avec les valeurs de rouge, vert, bleu et alpha fournies.</span><span class="sxs-lookup"><span data-stu-id="f63c3-104">Initializes a color with the supplied red, green, blue, and alpha values.</span></span>

## <a name="syntax"></a><span data-ttu-id="f63c3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f63c3-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_RGBA(
   int r,
   int g,
   int b,
   int a
);
```



## <a name="parameters"></a><span data-ttu-id="f63c3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f63c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f63c3-107">*r*</span><span class="sxs-lookup"><span data-stu-id="f63c3-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="f63c3-108">Composant rouge de la couleur.</span><span class="sxs-lookup"><span data-stu-id="f63c3-108">Red component of the color.</span></span> <span data-ttu-id="f63c3-109">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="f63c3-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="f63c3-110">*activée*</span><span class="sxs-lookup"><span data-stu-id="f63c3-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="f63c3-111">Composant vert de la couleur.</span><span class="sxs-lookup"><span data-stu-id="f63c3-111">Green component of the color.</span></span> <span data-ttu-id="f63c3-112">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="f63c3-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="f63c3-113">*b*</span><span class="sxs-lookup"><span data-stu-id="f63c3-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="f63c3-114">Composant bleu de la couleur.</span><span class="sxs-lookup"><span data-stu-id="f63c3-114">Blue component of the color.</span></span> <span data-ttu-id="f63c3-115">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="f63c3-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="f63c3-116">*un*</span><span class="sxs-lookup"><span data-stu-id="f63c3-116">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="f63c3-117">Composant alpha de la couleur.</span><span class="sxs-lookup"><span data-stu-id="f63c3-117">Alpha component of the color.</span></span> <span data-ttu-id="f63c3-118">Cette valeur doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="f63c3-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f63c3-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f63c3-119">Return value</span></span>

<span data-ttu-id="f63c3-120">Retourne la valeur [**D3DCOLOR**](d3dcolor.md) qui correspond aux valeurs RVBA fournies.</span><span class="sxs-lookup"><span data-stu-id="f63c3-120">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGBA values.</span></span>

## <a name="requirements"></a><span data-ttu-id="f63c3-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f63c3-121">Requirements</span></span>



| <span data-ttu-id="f63c3-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f63c3-122">Requirement</span></span> | <span data-ttu-id="f63c3-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f63c3-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f63c3-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f63c3-124">Header</span></span><br/> | <dl> <span data-ttu-id="f63c3-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f63c3-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f63c3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f63c3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f63c3-127">Macros</span><span class="sxs-lookup"><span data-stu-id="f63c3-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="f63c3-128">**D3DCOLOR \_ ARGB**</span><span class="sxs-lookup"><span data-stu-id="f63c3-128">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="f63c3-129">**D3DCOLOR \_ XRGB**</span><span class="sxs-lookup"><span data-stu-id="f63c3-129">**D3DCOLOR\_XRGB**</span></span>](d3dcolor-xrgb.md)
</dt> </dl>

 

 




