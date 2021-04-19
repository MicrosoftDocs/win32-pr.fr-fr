---
description: Décrit la résolution de la mémoire tampon z de l’ombre qui sera utilisée dans la simulation d’éclairage direct luminance Transfer (PRT) précalculé sur le GPU.
ms.assetid: 05354328-9b6f-45f5-a913-47ede170b03f
title: Énumération D3DXSHGPUSIMOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHGPUSIMOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a94845faf4c34657f486cfa371c5d41a12dc4336
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520341"
---
# <a name="d3dxshgpusimopt-enumeration"></a><span data-ttu-id="0feea-103">Énumération D3DXSHGPUSIMOPT</span><span class="sxs-lookup"><span data-stu-id="0feea-103">D3DXSHGPUSIMOPT enumeration</span></span>

<span data-ttu-id="0feea-104">Décrit la résolution de la mémoire tampon z de l’ombre qui sera utilisée dans la simulation d’éclairage direct luminance Transfer (PRT) précalculé sur le GPU.</span><span class="sxs-lookup"><span data-stu-id="0feea-104">Describes the resolution of the shadow z-buffer that will be used in Precomputed Radiance Transfer (PRT) direct lighting simulation on the GPU.</span></span> <span data-ttu-id="0feea-105">Une mémoire tampon z de qualité supérieure peut également être spécifiée pour réduire le bruit dans les résultats de la simulation d’éclairage direct, même si la simulation est plus lente.</span><span class="sxs-lookup"><span data-stu-id="0feea-105">A higher quality z-buffer can also be specified to reduce noise in the results of the direct lighting simulation, although the simulation will be slower.</span></span>

## <a name="syntax"></a><span data-ttu-id="0feea-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0feea-106">Syntax</span></span>


```C++
typedef enum D3DXSHGPUSIMOPT { 
  D3DXSHGPUSIMOPT_SHADOWRES256   = 1,
  D3DXSHGPUSIMOPT_SHADOWRES512   = 0,
  D3DXSHGPUSIMOPT_SHADOWRES1024  = 2,
  D3DXSHGPUSIMOPT_SHADOWRES2048  = 3,
  D3DXSHGPUSIMOPT_HIGHQUALITY    = 4,
  D3DXSHGPUSIMOPT_FORCE_DWORD    = 0x7fffffff
} D3DXSHGPUSIMOPT, *LPD3DXSHGPUSIMOPT;
```



## <a name="constants"></a><span data-ttu-id="0feea-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="0feea-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0feea-108"><span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES256**</span><span class="sxs-lookup"><span data-stu-id="0feea-108"><span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT\_SHADOWRES256**</span></span>
</dt> <dd>

<span data-ttu-id="0feea-109">Simulation de faible résolution.</span><span class="sxs-lookup"><span data-stu-id="0feea-109">Low resolution simulation.</span></span> <span data-ttu-id="0feea-110">Une texture de 256 x 256 pixels est utilisée dans la simulation pour encoder la mémoire tampon z de l’ombre.</span><span class="sxs-lookup"><span data-stu-id="0feea-110">A 256 x 256 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0feea-111"><span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES512**</span><span class="sxs-lookup"><span data-stu-id="0feea-111"><span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT\_SHADOWRES512**</span></span>
</dt> <dd>

<span data-ttu-id="0feea-112">Simulation de résolution moyenne.</span><span class="sxs-lookup"><span data-stu-id="0feea-112">Medium resolution simulation.</span></span> <span data-ttu-id="0feea-113">Une texture de 512 x 512 pixels est utilisée dans la simulation pour encoder la mémoire tampon z de l’ombre.</span><span class="sxs-lookup"><span data-stu-id="0feea-113">A 512 x 512 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span> <span data-ttu-id="0feea-114">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="0feea-114">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="0feea-115"><span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES1024**</span><span class="sxs-lookup"><span data-stu-id="0feea-115"><span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT\_SHADOWRES1024**</span></span>
</dt> <dd>

<span data-ttu-id="0feea-116">Simulation haute résolution.</span><span class="sxs-lookup"><span data-stu-id="0feea-116">High resolution simulation.</span></span> <span data-ttu-id="0feea-117">Une texture de 1024 x 1024 pixels est utilisée dans la simulation pour encoder la mémoire tampon z de l’ombre.</span><span class="sxs-lookup"><span data-stu-id="0feea-117">A 1024 x 1024 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0feea-118"><span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES2048**</span><span class="sxs-lookup"><span data-stu-id="0feea-118"><span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT\_SHADOWRES2048**</span></span>
</dt> <dd>

<span data-ttu-id="0feea-119">Simulation de résolution la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="0feea-119">Highest resolution simulation.</span></span> <span data-ttu-id="0feea-120">Une texture de 2048 x 2048 pixels est utilisée dans la simulation pour encoder la mémoire tampon z de l’ombre.</span><span class="sxs-lookup"><span data-stu-id="0feea-120">A 2048 x 2048 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0feea-121"><span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT \_ highquality**</span><span class="sxs-lookup"><span data-stu-id="0feea-121"><span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT\_HIGHQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="0feea-122">La simulation est de haute précision, quelle que soit la résolution sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="0feea-122">The simulation is of high precision, regardless of the selected resolution.</span></span> <span data-ttu-id="0feea-123">La définition de cette valeur permet de réduire le bruit dans les résultats de la simulation d’éclairage direct, même si la simulation est plus lente.</span><span class="sxs-lookup"><span data-stu-id="0feea-123">Setting this value will reduce noise in the results of the direct lighting simulation, although the simulation will be slower.</span></span> <span data-ttu-id="0feea-124">Peut être combiné avec l’une des valeurs de résolution.</span><span class="sxs-lookup"><span data-stu-id="0feea-124">May be combined with one of the resolution values.</span></span>

</dd> <dt>

<span data-ttu-id="0feea-125"><span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0feea-125"><span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="0feea-126">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="0feea-126">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="0feea-127">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0feea-127">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="0feea-128">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0feea-128">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0feea-129">Notes</span><span class="sxs-lookup"><span data-stu-id="0feea-129">Remarks</span></span>

<span data-ttu-id="0feea-130">Une seule des valeurs de résolution peut être spécifiée et peut être combinée avec la valeur de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="0feea-130">Only one of the resolution values may be specified, and may be combined with the high-quality value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0feea-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0feea-131">Requirements</span></span>



| <span data-ttu-id="0feea-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0feea-132">Requirement</span></span> | <span data-ttu-id="0feea-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="0feea-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0feea-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="0feea-134">Header</span></span><br/> | <dl> <span data-ttu-id="0feea-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0feea-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0feea-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0feea-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0feea-137">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="0feea-137">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




