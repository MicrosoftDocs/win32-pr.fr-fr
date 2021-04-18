---
description: Obtient l’emplacement actuel dans la largeur, la hauteur et la profondeur obtenues avec la valeur système [**DispatchRaysDimensions**](dispatchraysdimensions.md) intrinsèque.
title: DispatchRaysIndex
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysIndex
api_type:
- NA
ms.openlocfilehash: aa26400c26aba4ee9e647bcd0a79bad3f3d52f7c
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2020
ms.locfileid: "106512763"
---
# <a name="dispatchraysindex"></a><span data-ttu-id="55666-103">DispatchRaysIndex</span><span class="sxs-lookup"><span data-stu-id="55666-103">DispatchRaysIndex</span></span>

<span data-ttu-id="55666-104">Obtient l’emplacement actuel dans la largeur, la hauteur et la profondeur obtenues avec la valeur système [**DispatchRaysDimensions**](dispatchraysdimensions.md) intrinsèque.</span><span class="sxs-lookup"><span data-stu-id="55666-104">Gets the current location within the width, height, and depth obtained with the [**DispatchRaysDimensions**](dispatchraysdimensions.md) system value intrinsic.</span></span>

## <a name="syntax"></a><span data-ttu-id="55666-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55666-105">Syntax</span></span>

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a><span data-ttu-id="55666-106">Notes</span><span class="sxs-lookup"><span data-stu-id="55666-106">Remarks</span></span>

<span data-ttu-id="55666-107">Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants.</span><span class="sxs-lookup"><span data-stu-id="55666-107">This function can be called from the following raytracing shader types.</span></span>

* [<span data-ttu-id="55666-108">**Tout nuanceur de correspondance**</span><span class="sxs-lookup"><span data-stu-id="55666-108">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="55666-109">**Nuanceur pouvant être appelé**</span><span class="sxs-lookup"><span data-stu-id="55666-109">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="55666-110">**Nuanceur de correspondance le plus proche**</span><span class="sxs-lookup"><span data-stu-id="55666-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="55666-111">**Nuanceur d’intersection**</span><span class="sxs-lookup"><span data-stu-id="55666-111">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="55666-112">**Nuanceur manque**</span><span class="sxs-lookup"><span data-stu-id="55666-112">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="55666-113">**Nuanceur de création de rayon**</span><span class="sxs-lookup"><span data-stu-id="55666-113">**Ray Generation Shader**</span></span>](ray-generation-shader.md)

## <a name="see-also"></a><span data-ttu-id="55666-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55666-114">See also</span></span>

* [<span data-ttu-id="55666-115">Référence HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="55666-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
