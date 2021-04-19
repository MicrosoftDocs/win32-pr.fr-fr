---
description: Valeur float représentant le point de terminaison paramétrique actuel pour le rayon.
ms.assetid: ''
title: RayTCurrent
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTCurrent
api_type:
- NA
ms.openlocfilehash: 4f090bab88c6be671ca0614255fd7bdebb0d1549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515372"
---
# <a name="raytcurrent"></a><span data-ttu-id="f2ae7-103">RayTCurrent</span><span class="sxs-lookup"><span data-stu-id="f2ae7-103">RayTCurrent</span></span>

<span data-ttu-id="f2ae7-104">Valeur float représentant le point de terminaison paramétrique actuel pour le rayon.</span><span class="sxs-lookup"><span data-stu-id="f2ae7-104">A float representing the current parametric ending point for the ray.</span></span>  

## <a name="syntax"></a><span data-ttu-id="f2ae7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2ae7-105">Syntax</span></span>

```
float RayTCurrent();

```


## <a name="remarks"></a><span data-ttu-id="f2ae7-106">Notes</span><span class="sxs-lookup"><span data-stu-id="f2ae7-106">Remarks</span></span>

<span data-ttu-id="f2ae7-107">**RayTCurrent** définit le point de terminaison actuel du rayon en fonction de la formule suivante : Origin + (direction \* RayTCurrent).</span><span class="sxs-lookup"><span data-stu-id="f2ae7-107">**RayTCurrent** defines the current ending point of the ray according to the following formula: Origin + (Direction \* RayTCurrent).</span></span>  <span data-ttu-id="f2ae7-108">L' *origine* et la *direction* peuvent être dans le monde ou dans l’espace d’objet, ce qui donne lieu à un point de terminaison de l’espace d’un monde ou d’un objet.</span><span class="sxs-lookup"><span data-stu-id="f2ae7-108">*Origin* and *Direction* may be in either world or object space, which results in either a world or an object space ending point.</span></span>

<span data-ttu-id="f2ae7-109">**RayTCurrent** est initialisé dans l’appel de [**TraceRay**](traceray-function.md) d’appel avec la valeur [**RayDesc :: Tmax**](raydesc.md) , puis est mis à jour pendant la requête de trace lorsque des intersections sont signalées (dans le cas échéant) et acceptées.</span><span class="sxs-lookup"><span data-stu-id="f2ae7-109">**RayTCurrent** is initialized in the call [**TraceRay**](traceray-function.md) call with the [**RayDesc::TMax**](raydesc.md) value and then is updated during the trace query as intersections are reported (in the any hit), and accepted.</span></span>

<span data-ttu-id="f2ae7-110">Dans le [nuanceur d’intersection](intersection-shader.md), il représente la distance à l’intersection la plus proche trouvée jusqu’à présent.</span><span class="sxs-lookup"><span data-stu-id="f2ae7-110">In the [intersection shader](intersection-shader.md), it represents the distance to the closest intersection found so far.</span></span>  <span data-ttu-id="f2ae7-111">Il sera mis à jour après () à la valeur cela fournie si l’accès a été accepté.</span><span class="sxs-lookup"><span data-stu-id="f2ae7-111">It will be updated after () to the THit value provided if the hit was accepted.</span></span>

<span data-ttu-id="f2ae7-112">Dans les [nuanceurs de présence](any-hit-shader.md), il représente la distance à laquelle l’intersection active est signalée.</span><span class="sxs-lookup"><span data-stu-id="f2ae7-112">In the [any hit shader](any-hit-shader.md), it represents the distance to the current intersection being reported.</span></span>

<span data-ttu-id="f2ae7-113">Dans le [nuanceur de correspondance le plus proche](closest-hit-shader.md), il s’agit de la distance à laquelle l’intersection la plus proche est acceptée.</span><span class="sxs-lookup"><span data-stu-id="f2ae7-113">In the [closest hit shader](closest-hit-shader.md), it represents the distance to the closest intersection accepted.</span></span>

<span data-ttu-id="f2ae7-114">Dans le [nuanceur d’échecs](miss-shader.md), il est égal à *Tmax* passé à l’appel **TraceRay** .</span><span class="sxs-lookup"><span data-stu-id="f2ae7-114">In the [miss shader](miss-shader.md), it is equal to *TMax* passed to the **TraceRay** call.</span></span>


<span data-ttu-id="f2ae7-115">Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :</span><span class="sxs-lookup"><span data-stu-id="f2ae7-115">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="f2ae7-116">**Tout nuanceur de correspondance**</span><span class="sxs-lookup"><span data-stu-id="f2ae7-116">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="f2ae7-117">**Nuanceur de correspondance le plus proche**</span><span class="sxs-lookup"><span data-stu-id="f2ae7-117">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="f2ae7-118">**Nuanceur d’intersection**</span><span class="sxs-lookup"><span data-stu-id="f2ae7-118">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="f2ae7-119">**Nuanceur manque**</span><span class="sxs-lookup"><span data-stu-id="f2ae7-119">**Miss Shader**</span></span>](miss-shader.md)





## <a name="see-also"></a><span data-ttu-id="f2ae7-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2ae7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ae7-121">Référence HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="f2ae7-121">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




