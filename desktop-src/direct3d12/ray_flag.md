---
description: Indicateurs passés à la fonction TraceRay pour remplacer la transparence, l’élimination et le comportement précoce.
ms.assetid: ''
title: Énumération RAY_FLAG
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 31d6a002e5f3f4eeb5f86e671be0904d61cb916d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514538"
---
# <a name="ray_flag-enumeration"></a><span data-ttu-id="1e6fb-103">\_Énumération d’indicateurs de rayon</span><span class="sxs-lookup"><span data-stu-id="1e6fb-103">RAY\_FLAG enumeration</span></span>

<span data-ttu-id="1e6fb-104">Indicateurs passés à la fonction [**TraceRay**](traceray-function.md) pour remplacer la transparence, l’élimination et le comportement précoce.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-104">Flags passed to the [**TraceRay**](traceray-function.md) function to override transparency, culling, and early-out behavior.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e6fb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e6fb-105">Syntax</span></span>


```
enum RAY_FLAG : uint
{
    RAY_FLAG_NONE                            = 0x00,
    RAY_FLAG_FORCE_OPAQUE                    = 0x01,
    RAY_FLAG_FORCE_NON_OPAQUE                = 0x02,
    RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH = 0x04,
    RAY_FLAG_SKIP_CLOSEST_HIT_SHADER         = 0x08,
    RAY_FLAG_CULL_BACK_FACING_TRIANGLES      = 0x10,
    RAY_FLAG_CULL_FRONT_FACING_TRIANGLES     = 0x20,
    RAY_FLAG_CULL_OPAQUE                     = 0x40,
    RAY_FLAG_CULL_NON_OPAQUE                 = 0x80,
}; 
```



## <a name="constants"></a><span data-ttu-id="1e6fb-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="1e6fb-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1e6fb-107"><span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**indicateur de rayon \_ \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="1e6fb-107"><span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**RAY\_FLAG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="1e6fb-108">Aucune option sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-108">No options selected.</span></span>

</dd> <dt>

<span data-ttu-id="1e6fb-109"><span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**indicateur de rayon \_ \_ force \_ opaque**</span><span class="sxs-lookup"><span data-stu-id="1e6fb-109"><span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**RAY\_FLAG\_FORCE\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="1e6fb-110">Toutes les intersections de rayon-primitive rencontrées dans un raytrace sont traitées comme opaques.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-110">All ray-primitive intersections encountered in a raytrace are treated as opaque.</span></span>  <span data-ttu-id="1e6fb-111">Par conséquent, aucun nuanceur n’est exécuté, que la géométrie d’accès spécifie ou non l' \_ indicateur de géométrie D3D12 RAYTRACING \_ \_ \_ opaque, et quels que soient les indicateurs d’instance sur l’instance qui a été atteint.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-111">So no any hit shaders will be executed regardless of whether or not the hit geometry specifies D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE, and regardless of the instance flags on the instance that was hit.</span></span>

<span data-ttu-id="1e6fb-112">Cet indicateur s’exclut mutuellement avec l’indicateur de rayon \_ \_ force \_ non opaque, l’élimination des indicateurs de \_ rayon \_ \_ \_ opaque et l’élimination des indicateurs de rayon \_ \_ \_ non \_ opaque.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-112">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_NON\_OPAQUE, RAY\_FLAG\_CULL\_OPAQUE and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="1e6fb-113"><span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**indicateur de rayon \_ \_ force \_ non \_ opaque**</span><span class="sxs-lookup"><span data-stu-id="1e6fb-113"><span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**RAY\_FLAG\_FORCE\_NON\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="1e6fb-114">Toutes les intersections de rayon-primitive rencontrées dans un raytrace sont traitées comme non opaques.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-114">All ray-primitive intersections encountered in a raytrace are treated as non-opaque.</span></span>  <span data-ttu-id="1e6fb-115">Ainsi, tous les nuanceurs de correspondance, s’ils sont présents, sont exécutés indépendamment du fait que la géométrie d’accès spécifie l' \_ \_ indicateur de géométrie D3D12 RAYTRACING \_ \_ opaque et quels que soient les indicateurs d’instance sur l’instance qui a été atteint.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-115">So any hit shaders, if present, will be executed regardless of whether or not the hit geometry specifies D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE, and regardless of the instance flags on the instance that was hit.</span></span>
<span data-ttu-id="1e6fb-116">Cet indicateur s’exclut mutuellement avec l’indicateur de rayon \_ \_ FORCE_ \OPAQUE, les indicateurs de rayon, \_ \_ \_ les éliminations opaques et les indicateurs de rayon \_ \_ \_ non \_ opaques.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-116">This flag is mutually exclusive with RAY\_FLAG\_FORCE_\OPAQUE, RAY\_FLAG\_CULL\_OPAQUE and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="1e6fb-117"><span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**\_indicateur \_ de rayon acceptant le \_ premier \_ accès et la \_ fin de la \_ \_ recherche**</span><span class="sxs-lookup"><span data-stu-id="1e6fb-117"><span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**RAY\_FLAG\_ACCEPT\_FIRST\_HIT\_AND\_END\_SEARCH**</span></span>
</dt> <dd>

<span data-ttu-id="1e6fb-118">La première intersection de la primitive de Ray rencontrée dans un raytrace entraîne automatiquement l’appel de **AcceptHitAndEndSearch** juste après le nuanceur de correspondance, y compris s’il n’existe aucun nuanceur de correspondance.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-118">The first ray-primitive intersection encountered in a raytrace automatically causes **AcceptHitAndEndSearch** to be called immediately after the any hit shader, including if there is no any hit shader.</span></span> 
 
<span data-ttu-id="1e6fb-119">La seule exception est lorsque le nuanceur d’accès précédent appelle **IgnoreHit**. dans ce cas, le rayon continue non affecté, de telle sorte que l’accès suivant devient un autre candidat pour être le premier accès.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-119">The only exception is when the preceding any hit shader calls **IgnoreHit**, in which case the ray continues unaffected such that the next hit becomes another candidate to be the first hit.</span></span>  <span data-ttu-id="1e6fb-120">Pour que cette exception s’applique, le nuanceur de correspondance doit réellement être exécuté.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-120">For this exception to apply, the any hit shader has to actually be executed.</span></span>  <span data-ttu-id="1e6fb-121">Par conséquent, si les nuanceurs de présence sont ignorés car l’accès est considéré comme opaque (par exemple, en raison de l’indicateur de rayon force opaque ou de l’indicateur de \_ \_ \_ \_ géométrie D3D12 RAYTRACING opaque \_ \_ \_ ou de l’indicateur d' \_ instance D3D12 RAYTRACING \_ \_ \_ opaque défini), **AcceptHitAndEndSearch** est appelé.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-121">So if the any hit shader is skipped because the hit is treated as opaque (e.g. due to RAY\_FLAG\_FORCE\_OPAQUE or D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE or D3D12\_RAYTRACING\_INSTANCE\_FLAG\_OPAQUE being set), then **AcceptHitAndEndSearch** is called.</span></span>

<span data-ttu-id="1e6fb-122">Si un nuanceur de correspondance le plus proche est présent lors du premier accès, il est appelé à moins que le nuanceur de l’indicateur de rayon \_ \_ \_ le plus proche \_ \_ soit également présent.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-122">If a closest hit shader is present at the first hit, it gets invoked unless RAY\_FLAG\_SKIP\_CLOSEST\_HIT\_SHADER is also present.</span></span>  <span data-ttu-id="1e6fb-123">L’accès trouvé est considéré comme « le plus proche », même si d’autres résultats potentiels qui peuvent être plus proches sur le rayon n’ont peut-être pas été visités.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-123">The one hit that was found is considered “closest”, even though other potential hits that might be closer on the ray may not have been visited.</span></span>

<span data-ttu-id="1e6fb-124">Une utilisation courante de cet indicateur concerne les ombres, où un seul accès doit être trouvé.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-124">A typical use for this flag is for shadows, where only a single hit needs to be found.</span></span>


</dd> <dt>

<span data-ttu-id="1e6fb-125"><span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**indicateur de rayon \_ \_ Ignorer \_ le \_ nuanceur atteint le plus proche \_**</span><span class="sxs-lookup"><span data-stu-id="1e6fb-125"><span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**RAY\_FLAG\_SKIP\_CLOSEST\_HIT\_SHADER**</span></span>
</dt> <dd>

<span data-ttu-id="1e6fb-126">Même si au moins un accès a été validé et si le groupe d’accès de l’accès le plus proche contient un nuanceur de correspondance le plus proche, ignorez l’exécution de ce nuanceur.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-126">Even if at least one hit has been committed, and the hit group for the closest hit contains a closest hit shader, skip execution of that shader.</span></span> 

</dd> <dt>

<span data-ttu-id="1e6fb-127"><span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**triangles de la réforme de l’indicateur de rayon \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1e6fb-127"><span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**RAY\_FLAG\_CULL\_BACK\_FACING\_TRIANGLES**</span></span>
</dt> <dd>

<span data-ttu-id="1e6fb-128">Active l’élimination des triangles retournés vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-128">Enables culling of back facing triangles.</span></span> <span data-ttu-id="1e6fb-129">Consultez **\_ indicateurs d' \_ instance \_ D3D12 RAYTRACING** pour sélectionner les triangles de retour, par instance.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-129">See **D3D12\_RAYTRACING\_INSTANCE\_FLAGS** for selecting which triangles are back facing, per-instance.</span></span>

<span data-ttu-id="1e6fb-130">Sur les instances qui spécifient \_ \_ \_ la désactivation de l’indicateur d’instance D3D12 RAYTRACING \_ \_ \_ , cet indicateur n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-130">On instances that specify D3D12\_RAYTRACING\_INSTANCE\_FLAG\_TRIANGLE\_CULL\_DISABLE, this flag has no effect.</span></span>

<span data-ttu-id="1e6fb-131">Sur les types Geometry autres que D3D12 \_ RAYTRACING \_ Geometry \_ type \_ diangles, cet indicateur n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-131">On geometry types other than D3D12\_RAYTRACING\_GEOMETRY\_TYPE\_TRIANGLES, this flag has no effect.</span></span>

<span data-ttu-id="1e6fb-132">Cet indicateur s’exclut mutuellement avec \_ les \_ \_ \_ triangles frontaux de Culling de l’indicateur de rayon \_ .</span><span class="sxs-lookup"><span data-stu-id="1e6fb-132">This flag is mutually exclusive with RAY\_FLAG\_CULL\_FRONT\_FACING\_TRIANGLES.</span></span>


</dd> <dt>

<span data-ttu-id="1e6fb-133"><span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**\_ \_ \_ triangles frontaux de Culling \_ \_ de l’indicateur de rayon**</span><span class="sxs-lookup"><span data-stu-id="1e6fb-133"><span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**RAY\_FLAG\_CULL\_FRONT\_FACING\_TRIANGLES**</span></span>
</dt> <dd>

<span data-ttu-id="1e6fb-134">Active l’élimination des triangles frontaux.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-134">Enables culling of front facing triangles.</span></span> <span data-ttu-id="1e6fb-135">Consultez **\_ indicateurs d' \_ instance \_ D3D12 RAYTRACING** pour sélectionner les triangles de retour, par instance.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-135">See **D3D12\_RAYTRACING\_INSTANCE\_FLAGS** for selecting which triangles are back facing, per-instance.</span></span>

<span data-ttu-id="1e6fb-136">Sur les instances qui spécifient \_ \_ \_ la désactivation de l’indicateur d’instance D3D12 RAYTRACING \_ \_ \_ , cet indicateur n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-136">On instances that specify D3D12\_RAYTRACING\_INSTANCE\_FLAG\_TRIANGLE\_CULL\_DISABLE, this flag has no effect.</span></span>

<span data-ttu-id="1e6fb-137">Sur les types Geometry autres que D3D12 \_ RAYTRACING \_ Geometry \_ type \_ diangles, cet indicateur n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-137">On geometry types other than D3D12\_RAYTRACING\_GEOMETRY\_TYPE\_TRIANGLES, this flag has no effect.</span></span>

<span data-ttu-id="1e6fb-138">Cet indicateur s’exclut mutuellement avec \_ les \_ \_ \_ \_ triangles de retour de l’indicateur de rayon.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-138">This flag is mutually exclusive with RAY\_FLAG\_CULL\_BACK\_FACING\_TRIANGLES.</span></span>


</dd> <dt>

<span data-ttu-id="1e6fb-139"><span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**indicateur de rayon d' \_ \_ élimination \_ opaque**</span><span class="sxs-lookup"><span data-stu-id="1e6fb-139"><span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**RAY\_FLAG\_CULL\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="1e6fb-140">Élimine toutes les primitives considérées comme opaques en fonction de leurs indicateurs Geometry et d’instance.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-140">Culls all primitives that are considered opaque based on their geometry and instance flags.</span></span>

<span data-ttu-id="1e6fb-141">Cet indicateur s’exclut mutuellement avec l’indicateur de rayon \_ \_ force \_ opaque, l' \_ indicateur Ray \_ force \_ non \_ opaque et l’élimination des indicateurs de rayon \_ \_ \_ non \_ opaque.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-141">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_OPAQUE, RAY\_FLAG\_FORCE\_NON\_OPAQUE, and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="1e6fb-142"><span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**élimination d’indicateur de rayon \_ \_ \_ non \_ opaque**</span><span class="sxs-lookup"><span data-stu-id="1e6fb-142"><span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**RAY\_FLAG\_CULL\_NON\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="1e6fb-143">Élimine toutes les primitives considérées comme non opaques en fonction de leurs indicateurs Geometry et d’instance.</span><span class="sxs-lookup"><span data-stu-id="1e6fb-143">Culls all primitives that are considered non-opaque based on their geometry and instance flags.</span></span>

<span data-ttu-id="1e6fb-144">Cet indicateur s’exclut mutuellement avec l’indicateur de rayon \_ \_ force \_ opaque, l' \_ indicateur \_ de rayon force \_ non \_ opaque et l' \_ élimination opaque des indicateurs de rayon \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1e6fb-144">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_OPAQUE, RAY\_FLAG\_FORCE\_NON\_OPAQUE, and RAY\_FLAG\_CULL\_OPAQUE.</span></span>


</dd>

## <a name="requirements"></a><span data-ttu-id="1e6fb-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e6fb-145">Requirements</span></span>



## <a name="see-also"></a><span data-ttu-id="1e6fb-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e6fb-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e6fb-147">Référence HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="1e6fb-147">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




