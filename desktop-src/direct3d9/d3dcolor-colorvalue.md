---
description: Initialise une couleur avec les valeurs à virgule flottante rouge, vert, bleu et alpha fournies.
ms.assetid: 61825e33-4150-47cd-97f2-2144434a45e2
title: Macro D3DCOLOR_COLORVALUE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_COLORVALUE
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 3d5bb780a5999d8931335da1e9f49ad8af88dc12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761954"
---
# <a name="d3dcolor_colorvalue-macro"></a><span data-ttu-id="16d98-103">D3DCOLOR \_ macro COLORVALUE</span><span class="sxs-lookup"><span data-stu-id="16d98-103">D3DCOLOR\_COLORVALUE macro</span></span>

<span data-ttu-id="16d98-104">Initialise une couleur avec les valeurs à virgule flottante rouge, vert, bleu et alpha fournies.</span><span class="sxs-lookup"><span data-stu-id="16d98-104">Initializes a color with the supplied red, green, blue, and alpha floating-point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="16d98-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16d98-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_COLORVALUE(
   float r,
   float g,
   float b,
   float a
);
```



## <a name="parameters"></a><span data-ttu-id="16d98-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16d98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16d98-107">*r*</span><span class="sxs-lookup"><span data-stu-id="16d98-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="16d98-108">Composant rouge de la couleur.</span><span class="sxs-lookup"><span data-stu-id="16d98-108">Red component of the color.</span></span> <span data-ttu-id="16d98-109">Cette valeur doit être une valeur à virgule flottante comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="16d98-109">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="16d98-110">*activée*</span><span class="sxs-lookup"><span data-stu-id="16d98-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="16d98-111">Composant vert de la couleur.</span><span class="sxs-lookup"><span data-stu-id="16d98-111">Green component of the color.</span></span> <span data-ttu-id="16d98-112">Cette valeur doit être une valeur à virgule flottante comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="16d98-112">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="16d98-113">*b*</span><span class="sxs-lookup"><span data-stu-id="16d98-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="16d98-114">Composant bleu de la couleur.</span><span class="sxs-lookup"><span data-stu-id="16d98-114">Blue component of the color.</span></span> <span data-ttu-id="16d98-115">Cette valeur doit être une valeur à virgule flottante comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="16d98-115">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="16d98-116">*un*</span><span class="sxs-lookup"><span data-stu-id="16d98-116">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="16d98-117">Composant alpha de la couleur.</span><span class="sxs-lookup"><span data-stu-id="16d98-117">Alpha component of the color.</span></span> <span data-ttu-id="16d98-118">Cette valeur doit être une valeur à virgule flottante comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="16d98-118">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16d98-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16d98-119">Return value</span></span>

<span data-ttu-id="16d98-120">Retourne la valeur [**D3DCOLOR**](d3dcolor.md) qui correspond aux valeurs RVBA fournies.</span><span class="sxs-lookup"><span data-stu-id="16d98-120">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGBA values.</span></span>

## <a name="requirements"></a><span data-ttu-id="16d98-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16d98-121">Requirements</span></span>



| <span data-ttu-id="16d98-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16d98-122">Requirement</span></span> | <span data-ttu-id="16d98-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="16d98-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16d98-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="16d98-124">Header</span></span><br/> | <dl> <span data-ttu-id="16d98-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="16d98-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16d98-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16d98-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16d98-127">Macros</span><span class="sxs-lookup"><span data-stu-id="16d98-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




