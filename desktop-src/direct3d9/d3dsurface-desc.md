---
description: Décrit une surface.
ms.assetid: fad8ffdb-36e5-4695-b343-e1315357c31a
title: Structure D3DSURFACE_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSURFACE_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6424bbe9b78532657670bc5cd9ad0705de89a3b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531529"
---
# <a name="d3dsurface_desc-structure"></a><span data-ttu-id="0828f-103">D3DSURFACE \_ desc, structure</span><span class="sxs-lookup"><span data-stu-id="0828f-103">D3DSURFACE\_DESC structure</span></span>

<span data-ttu-id="0828f-104">Décrit une surface.</span><span class="sxs-lookup"><span data-stu-id="0828f-104">Describes a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0828f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0828f-105">Syntax</span></span>


```C++
typedef struct D3DSURFACE_DESC {
  D3DFORMAT           Format;
  D3DRESOURCETYPE     Type;
  DWORD               Usage;
  D3DPOOL             Pool;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  UINT                Width;
  UINT                Height;
} D3DSURFACE_DESC, *LPD3DSURFACE_DESC;
```



## <a name="members"></a><span data-ttu-id="0828f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="0828f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0828f-107">**Format**</span><span class="sxs-lookup"><span data-stu-id="0828f-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="0828f-108">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="0828f-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0828f-109">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de surface.</span><span class="sxs-lookup"><span data-stu-id="0828f-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format.</span></span>

</dd> <dt>

<span data-ttu-id="0828f-110">**Type**</span><span class="sxs-lookup"><span data-stu-id="0828f-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="0828f-111">Type : **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="0828f-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0828f-112">Membre du type énuméré [**D3DRESOURCETYPE**](./d3dresourcetype.md) , identifiant cette ressource comme une surface.</span><span class="sxs-lookup"><span data-stu-id="0828f-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a surface.</span></span>

</dd> <dt>

<span data-ttu-id="0828f-113">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="0828f-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="0828f-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0828f-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0828f-115">\_Valeurs D3DUSAGE DEPTHSTENCIL ou D3DUSAGE \_ RENDERTARGET.</span><span class="sxs-lookup"><span data-stu-id="0828f-115">Either the D3DUSAGE\_DEPTHSTENCIL or D3DUSAGE\_RENDERTARGET values.</span></span> <span data-ttu-id="0828f-116">Pour plus d’informations, consultez [**D3DUSAGE**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="0828f-116">For more information, see [**D3DUSAGE**](d3dusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="0828f-117">**Pool**</span><span class="sxs-lookup"><span data-stu-id="0828f-117">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="0828f-118">Type : **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="0828f-118">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0828f-119">Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , spécifiant la classe de mémoire allouée pour cette surface.</span><span class="sxs-lookup"><span data-stu-id="0828f-119">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this surface.</span></span>

</dd> <dt>

<span data-ttu-id="0828f-120">**MultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="0828f-120">**MultiSampleType**</span></span>
</dt> <dd>

<span data-ttu-id="0828f-121">Type : **[ **D3DMULTISAMPLE \_**](./d3dmultisample-type.md)**</span><span class="sxs-lookup"><span data-stu-id="0828f-121">Type: **[**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0828f-122">Membre du type [**énuméré \_ D3DMULTISAMPLE**](./d3dmultisample-type.md) , en spécifiant les niveaux d’échantillonnage multiple de la scène intégrale pris en charge par l’aire.</span><span class="sxs-lookup"><span data-stu-id="0828f-122">Member of the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type, specifying the levels of full-scene multisampling supported by the surface.</span></span>

</dd> <dt>

<span data-ttu-id="0828f-123">**MultiSampleQuality**</span><span class="sxs-lookup"><span data-stu-id="0828f-123">**MultiSampleQuality**</span></span>
</dt> <dd>

<span data-ttu-id="0828f-124">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0828f-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0828f-125">Niveau de qualité.</span><span class="sxs-lookup"><span data-stu-id="0828f-125">Quality level.</span></span> <span data-ttu-id="0828f-126">La plage valide est comprise entre zéro et un de moins que le niveau retourné par pQualityLevels utilisé par [**CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span><span class="sxs-lookup"><span data-stu-id="0828f-126">The valid range is between zero and one less than the level returned by pQualityLevels used by [**CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span></span> <span data-ttu-id="0828f-127">La transmission d’une valeur supérieure retourne l’erreur D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0828f-127">Passing a larger value returns the error, D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="0828f-128">Les valeurs MultisampleQuality des cibles de rendu jumelées, des surfaces du stencil de profondeur et du type d’échantillonnage multigraphique doivent toutes correspondre.</span><span class="sxs-lookup"><span data-stu-id="0828f-128">The MultisampleQuality values of paired render targets, depth stencil surfaces and the MultiSample type must all match.</span></span>

</dd> <dt>

<span data-ttu-id="0828f-129">**Width**</span><span class="sxs-lookup"><span data-stu-id="0828f-129">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="0828f-130">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0828f-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0828f-131">Largeur de la surface, en pixels.</span><span class="sxs-lookup"><span data-stu-id="0828f-131">Width of the surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0828f-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="0828f-132">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="0828f-133">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0828f-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0828f-134">Hauteur de la surface, en pixels.</span><span class="sxs-lookup"><span data-stu-id="0828f-134">Height of the surface, in pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0828f-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0828f-135">Requirements</span></span>



| <span data-ttu-id="0828f-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0828f-136">Requirement</span></span> | <span data-ttu-id="0828f-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="0828f-137">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0828f-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="0828f-138">Header</span></span><br/> | <dl> <span data-ttu-id="0828f-139"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="0828f-139"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0828f-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0828f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0828f-141">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="0828f-141">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="0828f-142">**GetLevelDesc**</span><span class="sxs-lookup"><span data-stu-id="0828f-142">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> <dt>

[<span data-ttu-id="0828f-143">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="0828f-143">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc)
</dt> <dt>

[<span data-ttu-id="0828f-144">**GetLevelDesc**</span><span class="sxs-lookup"><span data-stu-id="0828f-144">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> </dl>

 

 
