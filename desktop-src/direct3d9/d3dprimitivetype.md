---
description: Définit les primitives prises en charge par Direct3D.
ms.assetid: 89e697f9-02b9-4ae1-9e86-6178da0cb008
title: Énumération D3DPRIMITIVETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRIMITIVETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 933bbec72950bd2c73fda8b3781dd46393ca4c96
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116242"
---
# <a name="d3dprimitivetype-enumeration"></a><span data-ttu-id="1d2a0-103">Énumération D3DPRIMITIVETYPE</span><span class="sxs-lookup"><span data-stu-id="1d2a0-103">D3DPRIMITIVETYPE enumeration</span></span>

<span data-ttu-id="1d2a0-104">Définit les primitives prises en charge par Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-104">Defines the primitives supported by Direct3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d2a0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d2a0-105">Syntax</span></span>


```C++
typedef enum D3DPRIMITIVETYPE { 
  D3DPT_POINTLIST      = 1,
  D3DPT_LINELIST       = 2,
  D3DPT_LINESTRIP      = 3,
  D3DPT_TRIANGLELIST   = 4,
  D3DPT_TRIANGLESTRIP  = 5,
  D3DPT_TRIANGLEFAN    = 6,
  D3DPT_FORCE_DWORD    = 0x7fffffff
} D3DPRIMITIVETYPE, *LPD3DPRIMITIVETYPE;
```



## <a name="constants"></a><span data-ttu-id="1d2a0-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="1d2a0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1d2a0-107"><span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT \_ POINTLIST**</span><span class="sxs-lookup"><span data-stu-id="1d2a0-107"><span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT\_POINTLIST**</span></span>
</dt> <dd>

<span data-ttu-id="1d2a0-108">Génère le rendu des vertex sous la forme d’une collection de points isolés.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-108">Renders the vertices as a collection of isolated points.</span></span> <span data-ttu-id="1d2a0-109">Cette valeur n’est pas prise en charge pour les primitives indexées.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-109">This value is unsupported for indexed primitives.</span></span>

</dd> <dt>

<span data-ttu-id="1d2a0-110"><span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**D3DPT \_ LINELIST**</span><span class="sxs-lookup"><span data-stu-id="1d2a0-110"><span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**D3DPT\_LINELIST**</span></span>
</dt> <dd>

<span data-ttu-id="1d2a0-111">Génère le rendu des vertex sous la forme d’une liste de segments de ligne droite isolés.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-111">Renders the vertices as a list of isolated straight line segments.</span></span>

</dd> <dt>

<span data-ttu-id="1d2a0-112"><span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**D3DPT \_ LINESTRIP**</span><span class="sxs-lookup"><span data-stu-id="1d2a0-112"><span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**D3DPT\_LINESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="1d2a0-113">Restitue les vertex sous la forme d’une polyligne unique.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-113">Renders the vertices as a single polyline.</span></span>

</dd> <dt>

<span data-ttu-id="1d2a0-114"><span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**D3DPT \_ TRIANGLELIST**</span><span class="sxs-lookup"><span data-stu-id="1d2a0-114"><span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**D3DPT\_TRIANGLELIST**</span></span>
</dt> <dd>

<span data-ttu-id="1d2a0-115">Génère le rendu des vertex spécifiés sous la forme d’une séquence de triangles isolés.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-115">Renders the specified vertices as a sequence of isolated triangles.</span></span> <span data-ttu-id="1d2a0-116">Chaque groupe de trois vertex définit un triangle distinct.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-116">Each group of three vertices defines a separate triangle.</span></span>

<span data-ttu-id="1d2a0-117">L’élimination de face arrière est affectée par l’état de rendu de l’ordre d’enroulement actuel.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-117">Back-face culling is affected by the current winding-order render state.</span></span>

</dd> <dt>

<span data-ttu-id="1d2a0-118"><span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**D3DPT \_ TRIANGLESTRIP**</span><span class="sxs-lookup"><span data-stu-id="1d2a0-118"><span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**D3DPT\_TRIANGLESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="1d2a0-119">Restitue les vertex sous la forme d’une bande triangulaire.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-119">Renders the vertices as a triangle strip.</span></span> <span data-ttu-id="1d2a0-120">L’indicateur de l’élimination des visages est automatiquement inversé sur les triangles pairs.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-120">The backface-culling flag is automatically flipped on even-numbered triangles.</span></span>

</dd> <dt>

<span data-ttu-id="1d2a0-121"><span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**D3DPT \_ TRIANGLEFAN**</span><span class="sxs-lookup"><span data-stu-id="1d2a0-121"><span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**D3DPT\_TRIANGLEFAN**</span></span>
</dt> <dd>

<span data-ttu-id="1d2a0-122">Restitue les vertex sous la forme d’un ventilateur triangulaire.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-122">Renders the vertices as a triangle fan.</span></span>

</dd> <dt>

<span data-ttu-id="1d2a0-123"><span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="1d2a0-123"><span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="1d2a0-124">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-124">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="1d2a0-125">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-125">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="1d2a0-126">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-126">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d2a0-127">Notes</span><span class="sxs-lookup"><span data-stu-id="1d2a0-127">Remarks</span></span>

<span data-ttu-id="1d2a0-128">L’utilisation de [barrettes](triangle-strips.md) triangulaires ou de [ventilateurs triangulaires (Direct3D 9)](triangle-fans.md) est souvent plus efficace que l’utilisation des listes de triangles, car moins de vertex sont dupliqués.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-128">Using [Triangle Strips](triangle-strips.md) or [Triangle Fans (Direct3D 9)](triangle-fans.md) is often more efficient than using triangle lists because fewer vertices are duplicated.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d2a0-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d2a0-129">Requirements</span></span>



| <span data-ttu-id="1d2a0-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d2a0-130">Requirement</span></span> | <span data-ttu-id="1d2a0-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d2a0-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d2a0-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d2a0-132">Header</span></span><br/> | <dl> <span data-ttu-id="1d2a0-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d2a0-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d2a0-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d2a0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d2a0-135">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="1d2a0-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="1d2a0-136">**IDirect3DDevice9 ::D rawIndexedPrimitive**</span><span class="sxs-lookup"><span data-stu-id="1d2a0-136">**IDirect3DDevice9::DrawIndexedPrimitive**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)
</dt> <dt>

[<span data-ttu-id="1d2a0-137">**IDirect3DDevice9 ::D rawIndexedPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="1d2a0-137">**IDirect3DDevice9::DrawIndexedPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)
</dt> <dt>

[<span data-ttu-id="1d2a0-138">**IDirect3DDevice9 ::D rawPrimitive**</span><span class="sxs-lookup"><span data-stu-id="1d2a0-138">**IDirect3DDevice9::DrawPrimitive**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)
</dt> <dt>

[<span data-ttu-id="1d2a0-139">**IDirect3DDevice9 ::D rawPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="1d2a0-139">**IDirect3DDevice9::DrawPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
</dt> </dl>

 

 
