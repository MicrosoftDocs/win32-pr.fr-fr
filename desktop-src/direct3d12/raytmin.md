---
description: Valeur float représentant le point de départ paramétrique actuel pour le rayon.
ms.assetid: ''
title: RayTMin
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTMin
api_type:
- NA
ms.openlocfilehash: 00db0eb46e8c011e5b31f773679e19ca6dd4a7a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544589"
---
# <a name="raytmin"></a><span data-ttu-id="e8519-103">RayTMin</span><span class="sxs-lookup"><span data-stu-id="e8519-103">RayTMin</span></span>

<span data-ttu-id="e8519-104">Valeur float représentant le point de départ paramétrique actuel pour le rayon.</span><span class="sxs-lookup"><span data-stu-id="e8519-104">A float representing the current parametric starting point for the ray.</span></span> 

## <a name="syntax"></a><span data-ttu-id="e8519-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8519-105">Syntax</span></span>

```
float RayTMin();

```

## <a name="remarks"></a><span data-ttu-id="e8519-106">Notes</span><span class="sxs-lookup"><span data-stu-id="e8519-106">Remarks</span></span>

<span data-ttu-id="e8519-107">**RayTMin** définit le point de départ du rayon en fonction de la formule suivante : Origin + (direction \* RayTMin).</span><span class="sxs-lookup"><span data-stu-id="e8519-107">**RayTMin** defines the starting point of the ray according to the following formula: Origin + (Direction \* RayTMin).</span></span>  <span data-ttu-id="e8519-108">L' *origine* et la *direction* peuvent être dans le monde ou dans l’espace d’objet, ce qui se traduit par un point de départ ou un espace d’objet.</span><span class="sxs-lookup"><span data-stu-id="e8519-108">*Origin* and *Direction* may be in either world or object space, which results in either a world or an object space starting point.</span></span>

<span data-ttu-id="e8519-109">**RayTMin** est spécifié dans l’appel à [**TraceRay**](traceray-function.md)et est constant pour la durée de cet appel.</span><span class="sxs-lookup"><span data-stu-id="e8519-109">**RayTMin** is specified in the call to [**TraceRay**](traceray-function.md), and is constant for the duration of that call.</span></span>




<span data-ttu-id="e8519-110">Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :</span><span class="sxs-lookup"><span data-stu-id="e8519-110">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="e8519-111">**Tout nuanceur de correspondance**</span><span class="sxs-lookup"><span data-stu-id="e8519-111">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="e8519-112">**Nuanceur de correspondance le plus proche**</span><span class="sxs-lookup"><span data-stu-id="e8519-112">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="e8519-113">**Nuanceur d’intersection**</span><span class="sxs-lookup"><span data-stu-id="e8519-113">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="e8519-114">**Nuanceur manque**</span><span class="sxs-lookup"><span data-stu-id="e8519-114">**Miss Shader**</span></span>](miss-shader.md)





## <a name="see-also"></a><span data-ttu-id="e8519-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8519-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8519-116">Référence HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="e8519-116">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




