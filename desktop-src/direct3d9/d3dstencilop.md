---
description: Définit les opérations de mémoire tampon de stencil.
ms.assetid: 338a3b7f-236a-484f-96b8-1e6bfb014484
title: Énumération D3DSTENCILOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTENCILOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 34784a57d3afd3862d380554040f3909ec905898
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523815"
---
# <a name="d3dstencilop-enumeration"></a><span data-ttu-id="b4435-103">Énumération D3DSTENCILOP</span><span class="sxs-lookup"><span data-stu-id="b4435-103">D3DSTENCILOP enumeration</span></span>

<span data-ttu-id="b4435-104">Définit les opérations de mémoire tampon de stencil.</span><span class="sxs-lookup"><span data-stu-id="b4435-104">Defines stencil-buffer operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4435-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4435-105">Syntax</span></span>


```C++
typedef enum D3DSTENCILOP { 
  D3DSTENCILOP_KEEP         = 1,
  D3DSTENCILOP_ZERO         = 2,
  D3DSTENCILOP_REPLACE      = 3,
  D3DSTENCILOP_INCRSAT      = 4,
  D3DSTENCILOP_DECRSAT      = 5,
  D3DSTENCILOP_INVERT       = 6,
  D3DSTENCILOP_INCR         = 7,
  D3DSTENCILOP_DECR         = 8,
  D3DSTENCILOP_FORCE_DWORD  = 0x7fffffff
} D3DSTENCILOP, *LPD3DSTENCILOP;
```



## <a name="constants"></a><span data-ttu-id="b4435-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b4435-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b4435-107"><span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP \_ conserver**</span><span class="sxs-lookup"><span data-stu-id="b4435-107"><span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP\_KEEP**</span></span>
</dt> <dd>

<span data-ttu-id="b4435-108">Ne mettez pas à jour l’entrée dans la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="b4435-108">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="b4435-109">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="b4435-109">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="b4435-110"><span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP \_ zéro**</span><span class="sxs-lookup"><span data-stu-id="b4435-110"><span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP\_ZERO**</span></span>
</dt> <dd>

<span data-ttu-id="b4435-111">Affectez à l’entrée de tampon stencil la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="b4435-111">Set the stencil-buffer entry to 0.</span></span>

</dd> <dt>

<span data-ttu-id="b4435-112"><span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP \_ remplacer**</span><span class="sxs-lookup"><span data-stu-id="b4435-112"><span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP\_REPLACE**</span></span>
</dt> <dd>

<span data-ttu-id="b4435-113">Remplacez l’entrée stencil-tampon par une valeur de référence.</span><span class="sxs-lookup"><span data-stu-id="b4435-113">Replace the stencil-buffer entry with a reference value.</span></span>

</dd> <dt>

<span data-ttu-id="b4435-114"><span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP \_ INCRSAT**</span><span class="sxs-lookup"><span data-stu-id="b4435-114"><span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP\_INCRSAT**</span></span>
</dt> <dd>

<span data-ttu-id="b4435-115">Incrémentez l’entrée de mémoire tampon du stencil, en la conservant à la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="b4435-115">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>

</dd> <dt>

<span data-ttu-id="b4435-116"><span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP \_ DECRSAT**</span><span class="sxs-lookup"><span data-stu-id="b4435-116"><span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP\_DECRSAT**</span></span>
</dt> <dd>

<span data-ttu-id="b4435-117">Décrémenter l’entrée de mémoire tampon du stencil, en la mettant à zéro.</span><span class="sxs-lookup"><span data-stu-id="b4435-117">Decrement the stencil-buffer entry, clamping to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b4435-118"><span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**D3DSTENCILOP \_ inversé**</span><span class="sxs-lookup"><span data-stu-id="b4435-118"><span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**D3DSTENCILOP\_INVERT**</span></span>
</dt> <dd>

<span data-ttu-id="b4435-119">Inversez les bits dans l’entrée de mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="b4435-119">Invert the bits in the stencil-buffer entry.</span></span>

</dd> <dt>

<span data-ttu-id="b4435-120"><span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**\_Incr D3DSTENCILOP**</span><span class="sxs-lookup"><span data-stu-id="b4435-120"><span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCILOP\_INCR**</span></span>
</dt> <dd>

<span data-ttu-id="b4435-121">Incrémente l’entrée de mémoire tampon du stencil, en renvoyant à zéro si la nouvelle valeur dépasse la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="b4435-121">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>

</dd> <dt>

<span data-ttu-id="b4435-122"><span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP \_ DECR (**</span><span class="sxs-lookup"><span data-stu-id="b4435-122"><span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP\_DECR**</span></span>
</dt> <dd>

<span data-ttu-id="b4435-123">Décrémente l’entrée de mémoire tampon du stencil, en renvoyant à la valeur maximale si la nouvelle valeur est inférieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="b4435-123">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span>

</dd> <dt>

<span data-ttu-id="b4435-124"><span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="b4435-124"><span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="b4435-125">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="b4435-125">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="b4435-126">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b4435-126">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="b4435-127">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="b4435-127">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4435-128">Notes</span><span class="sxs-lookup"><span data-stu-id="b4435-128">Remarks</span></span>

<span data-ttu-id="b4435-129">Les entrées de mémoire tampon de stencil sont des valeurs entières comprises entre 0 et 2 ⁿ-1, où n est la profondeur en bits de la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="b4435-129">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4435-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4435-130">Requirements</span></span>



| <span data-ttu-id="b4435-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4435-131">Requirement</span></span> | <span data-ttu-id="b4435-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4435-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4435-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4435-133">Header</span></span><br/> | <dl> <span data-ttu-id="b4435-134"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4435-134"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4435-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4435-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4435-136">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="b4435-136">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




