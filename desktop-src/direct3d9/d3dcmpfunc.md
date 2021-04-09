---
description: Définit les fonctions de comparaison prises en charge.
ms.assetid: 999af3eb-a208-4312-acee-373192ea69e4
title: Énumération D3DCMPFUNC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCMPFUNC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e49f0e058e795e00349020619f1e6d6310dfd94f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870090"
---
# <a name="d3dcmpfunc-enumeration"></a><span data-ttu-id="c59b0-103">Énumération D3DCMPFUNC</span><span class="sxs-lookup"><span data-stu-id="c59b0-103">D3DCMPFUNC enumeration</span></span>

<span data-ttu-id="c59b0-104">Définit les fonctions de comparaison prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c59b0-104">Defines the supported compare functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c59b0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c59b0-105">Syntax</span></span>


```C++
typedef enum D3DCMPFUNC { 
  D3DCMP_NEVER         = 1,
  D3DCMP_LESS          = 2,
  D3DCMP_EQUAL         = 3,
  D3DCMP_LESSEQUAL     = 4,
  D3DCMP_GREATER       = 5,
  D3DCMP_NOTEQUAL      = 6,
  D3DCMP_GREATEREQUAL  = 7,
  D3DCMP_ALWAYS        = 8,
  D3DCMP_FORCE_DWORD   = 0x7fffffff
} D3DCMPFUNC, *LPD3DCMPFUNC;
```



## <a name="constants"></a><span data-ttu-id="c59b0-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c59b0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c59b0-107"><span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP \_ jamais**</span><span class="sxs-lookup"><span data-stu-id="c59b0-107"><span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP\_NEVER**</span></span>
</dt> <dd>

<span data-ttu-id="c59b0-108">Toujours faire échouer le test.</span><span class="sxs-lookup"><span data-stu-id="c59b0-108">Always fail the test.</span></span>

</dd> <dt>

<span data-ttu-id="c59b0-109"><span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP \_ moins**</span><span class="sxs-lookup"><span data-stu-id="c59b0-109"><span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP\_LESS**</span></span>
</dt> <dd>

<span data-ttu-id="c59b0-110">Accepter le nouveau pixel si sa valeur est inférieure à la valeur du pixel actuel.</span><span class="sxs-lookup"><span data-stu-id="c59b0-110">Accept the new pixel if its value is less than the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="c59b0-111"><span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP \_ égal à**</span><span class="sxs-lookup"><span data-stu-id="c59b0-111"><span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP\_EQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="c59b0-112">Accepter le nouveau pixel si sa valeur est égale à la valeur du pixel actuel.</span><span class="sxs-lookup"><span data-stu-id="c59b0-112">Accept the new pixel if its value equals the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="c59b0-113"><span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP \_ LESSEQUAL**</span><span class="sxs-lookup"><span data-stu-id="c59b0-113"><span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP\_LESSEQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="c59b0-114">Accepter le nouveau pixel si sa valeur est inférieure ou égale à la valeur du pixel actuel.</span><span class="sxs-lookup"><span data-stu-id="c59b0-114">Accept the new pixel if its value is less than or equal to the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="c59b0-115"><span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP \_ plus**</span><span class="sxs-lookup"><span data-stu-id="c59b0-115"><span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP\_GREATER**</span></span>
</dt> <dd>

<span data-ttu-id="c59b0-116">Accepter le nouveau pixel si sa valeur est supérieure à la valeur du pixel actuel.</span><span class="sxs-lookup"><span data-stu-id="c59b0-116">Accept the new pixel if its value is greater than the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="c59b0-117"><span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**D3DCMP \_ NOTEQUAL**</span><span class="sxs-lookup"><span data-stu-id="c59b0-117"><span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**D3DCMP\_NOTEQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="c59b0-118">Accepter le nouveau pixel si sa valeur n’est pas égale à la valeur du pixel actuel.</span><span class="sxs-lookup"><span data-stu-id="c59b0-118">Accept the new pixel if its value does not equal the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="c59b0-119"><span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP \_ greaterequal à**</span><span class="sxs-lookup"><span data-stu-id="c59b0-119"><span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP\_GREATEREQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="c59b0-120">Accepter le nouveau pixel si sa valeur est supérieure ou égale à la valeur du pixel actuel.</span><span class="sxs-lookup"><span data-stu-id="c59b0-120">Accept the new pixel if its value is greater than or equal to the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="c59b0-121"><span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP \_ toujours**</span><span class="sxs-lookup"><span data-stu-id="c59b0-121"><span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP\_ALWAYS**</span></span>
</dt> <dd>

<span data-ttu-id="c59b0-122">Passe toujours le test.</span><span class="sxs-lookup"><span data-stu-id="c59b0-122">Always pass the test.</span></span>

</dd> <dt>

<span data-ttu-id="c59b0-123"><span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c59b0-123"><span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="c59b0-124">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="c59b0-124">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="c59b0-125">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c59b0-125">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="c59b0-126">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c59b0-126">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c59b0-127">Notes</span><span class="sxs-lookup"><span data-stu-id="c59b0-127">Remarks</span></span>

<span data-ttu-id="c59b0-128">Les valeurs de ce type énuméré définissent les fonctions de comparaison prises en charge pour les \_ États de rendu D3DRS ZFUNC, D3DRS \_ ALPHAFUNC et D3DRS \_ STENCILFUNC.</span><span class="sxs-lookup"><span data-stu-id="c59b0-128">The values in this enumerated type define the supported compare functions for the D3DRS\_ZFUNC, D3DRS\_ALPHAFUNC, and D3DRS\_STENCILFUNC render states.</span></span>

## <a name="requirements"></a><span data-ttu-id="c59b0-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c59b0-129">Requirements</span></span>



| <span data-ttu-id="c59b0-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c59b0-130">Requirement</span></span> | <span data-ttu-id="c59b0-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c59b0-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c59b0-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="c59b0-132">Header</span></span><br/> | <dl> <span data-ttu-id="c59b0-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c59b0-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c59b0-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c59b0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c59b0-135">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="c59b0-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="c59b0-136">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="c59b0-136">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
