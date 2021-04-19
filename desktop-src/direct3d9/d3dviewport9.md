---
description: Définit les dimensions de la fenêtre d’une surface de cible de rendu sur laquelle un projet de volume 3D.
ms.assetid: fb2c6048-f837-497d-8e4f-e18942d37899
title: D3DVIEWPORT9, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVIEWPORT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3d96000de50934ebdc893ffc3866dd3252703bdc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522366"
---
# <a name="d3dviewport9-structure"></a><span data-ttu-id="4f0cf-103">D3DVIEWPORT9, structure</span><span class="sxs-lookup"><span data-stu-id="4f0cf-103">D3DVIEWPORT9 structure</span></span>

<span data-ttu-id="4f0cf-104">Définit les dimensions de la fenêtre d’une surface de cible de rendu sur laquelle un projet de volume 3D.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-104">Defines the window dimensions of a render-target surface onto which a 3D volume projects.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f0cf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f0cf-105">Syntax</span></span>


```C++
typedef struct D3DVIEWPORT9 {
  DWORD X;
  DWORD Y;
  DWORD Width;
  DWORD Height;
  float MinZ;
  float MaxZ;
} D3DVIEWPORT9, *LPD3DVIEWPORT9;
```



## <a name="members"></a><span data-ttu-id="4f0cf-106">Membres</span><span class="sxs-lookup"><span data-stu-id="4f0cf-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4f0cf-107">**X**</span><span class="sxs-lookup"><span data-stu-id="4f0cf-107">**X**</span></span>
</dt> <dd>

<span data-ttu-id="4f0cf-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f0cf-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f0cf-109">Coordonnée de pixels de l’angle supérieur gauche de la fenêtre d’affichage sur la surface de rendu-cible.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-109">Pixel coordinate of the upper-left corner of the viewport on the render-target surface.</span></span> <span data-ttu-id="4f0cf-110">À moins que vous ne souhaitiez effectuer un rendu sur un sous-ensemble de la surface, ce membre peut être défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-110">Unless you want to render to a subset of the surface, this member can be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="4f0cf-111">**O**</span><span class="sxs-lookup"><span data-stu-id="4f0cf-111">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="4f0cf-112">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f0cf-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f0cf-113">Coordonnée de pixels de l’angle supérieur gauche de la fenêtre d’affichage sur la surface de rendu-cible.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-113">Pixel coordinate of the upper-left corner of the viewport on the render-target surface.</span></span> <span data-ttu-id="4f0cf-114">À moins que vous ne souhaitiez effectuer un rendu sur un sous-ensemble de la surface, ce membre peut être défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-114">Unless you want to render to a subset of the surface, this member can be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="4f0cf-115">**Width**</span><span class="sxs-lookup"><span data-stu-id="4f0cf-115">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="4f0cf-116">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f0cf-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f0cf-117">Largeur de la dimension du volume du clip, en pixels.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-117">Width dimension of the clip volume, in pixels.</span></span> <span data-ttu-id="4f0cf-118">À moins que vous ne soyez rendu qu’à un sous-ensemble de la surface, ce membre doit être défini sur la dimension de largeur de la surface de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-118">Unless you are rendering only to a subset of the surface, this member should be set to the width dimension of the render-target surface.</span></span>

</dd> <dt>

<span data-ttu-id="4f0cf-119">**Height**</span><span class="sxs-lookup"><span data-stu-id="4f0cf-119">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="4f0cf-120">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f0cf-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f0cf-121">Dimension de hauteur du volume du clip, en pixels.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-121">Height dimension of the clip volume, in pixels.</span></span> <span data-ttu-id="4f0cf-122">À moins d’être rendu uniquement à un sous-ensemble de la surface, ce membre doit être défini sur la dimension de hauteur de la surface de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-122">Unless you are rendering only to a subset of the surface, this member should be set to the height dimension of the render-target surface.</span></span>

</dd> <dt>

<span data-ttu-id="4f0cf-123">**MinZ**</span><span class="sxs-lookup"><span data-stu-id="4f0cf-123">**MinZ**</span></span>
</dt> <dd>

<span data-ttu-id="4f0cf-124">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="4f0cf-124">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="4f0cf-125">Avec MaxZ, valeur décrivant la plage de valeurs de profondeur dans laquelle une scène doit être rendue, les valeurs minimales et maximales du volume de clip.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-125">Together with MaxZ, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume.</span></span> <span data-ttu-id="4f0cf-126">La plupart des applications définissent cette valeur sur 0,0.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-126">Most applications set this value to 0.0.</span></span> <span data-ttu-id="4f0cf-127">Le découpage est effectué après l’application de la matrice de projection.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-127">Clipping is performed after applying the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="4f0cf-128">**MaxZ**</span><span class="sxs-lookup"><span data-stu-id="4f0cf-128">**MaxZ**</span></span>
</dt> <dd>

<span data-ttu-id="4f0cf-129">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="4f0cf-129">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="4f0cf-130">Avec MinZ, valeur décrivant la plage de valeurs de profondeur dans laquelle une scène doit être rendue, les valeurs minimales et maximales du volume de clip.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-130">Together with MinZ, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume.</span></span> <span data-ttu-id="4f0cf-131">La plupart des applications définissent cette valeur sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-131">Most applications set this value to 1.0.</span></span> <span data-ttu-id="4f0cf-132">Le découpage est effectué après l’application de la matrice de projection.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-132">Clipping is performed after applying the projection matrix.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f0cf-133">Notes</span><span class="sxs-lookup"><span data-stu-id="4f0cf-133">Remarks</span></span>

<span data-ttu-id="4f0cf-134">Les membres X, Y, Width et Height décrivent la position et les dimensions de la fenêtre d’affichage sur la surface de rendu-cible.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-134">The X, Y, Width, and Height members describe the position and dimensions of the viewport on the render-target surface.</span></span> <span data-ttu-id="4f0cf-135">En règle générale, les applications sont rendues sur l’ensemble de la surface cible. lors du rendu sur une surface 640 x 480, ces membres doivent être respectivement 0, 0, 640 et 480.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-135">Usually, applications render to the entire target surface; when rendering on a 640 x 480 surface, these members should be 0, 0, 640, and 480, respectively.</span></span> <span data-ttu-id="4f0cf-136">MinZ et MaxZ sont généralement définis sur 0,0 et 1,0, mais peuvent être définis sur d’autres valeurs pour obtenir des effets spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-136">The MinZ and MaxZ are typically set to 0.0 and 1.0 but can be set to other values to achieve specific effects.</span></span> <span data-ttu-id="4f0cf-137">Par exemple, vous pouvez les définir à la fois sur 0,0 pour forcer le système à restituer les objets au premier plan d’une scène, ou les deux à 1,0 pour forcer les objets en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-137">For example, you might set them both to 0.0 to force the system to render objects to the foreground of a scene, or both to 1.0 to force the objects into the background.</span></span>

<span data-ttu-id="4f0cf-138">Lorsque les paramètres de la fenêtre d’affichage d’un appareil changent (en raison d’un appel à la méthode [**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) ), le pilote crée une nouvelle matrice de transformation.</span><span class="sxs-lookup"><span data-stu-id="4f0cf-138">When the viewport parameters for a device change (because of a call to the [**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) method), the driver builds a new transformation matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f0cf-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f0cf-139">Requirements</span></span>



| <span data-ttu-id="4f0cf-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f0cf-140">Requirement</span></span> | <span data-ttu-id="4f0cf-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f0cf-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f0cf-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f0cf-142">Header</span></span><br/> | <dl> <span data-ttu-id="4f0cf-143"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f0cf-143"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f0cf-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f0cf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f0cf-145">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="4f0cf-145">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="4f0cf-146">**GetViewport**</span><span class="sxs-lookup"><span data-stu-id="4f0cf-146">**GetViewport**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
</dt> <dt>

[<span data-ttu-id="4f0cf-147">**SetViewport**</span><span class="sxs-lookup"><span data-stu-id="4f0cf-147">**SetViewport**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)
</dt> </dl>

 

 
