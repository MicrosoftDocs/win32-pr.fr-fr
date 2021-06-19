---
title: Intrinsèques de valeur système HLSL Direct3D 12 Raytracing
description: Affichez des liens vers des articles décrivant les fonctions intrinsèques de valeur système HLSL (High-Level Shader Language) qui prennent en charge le pipeline Raytracing Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2790cf5df42f64071db3ca51a35e58ee9afcd5
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396434"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a><span data-ttu-id="09b15-103">Intrinsèques de valeur système HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="09b15-103">Direct3D 12 raytracing HLSL system value intrinsics</span></span>

<span data-ttu-id="09b15-104">Les valeurs système sont extraites à l’aide de fonctions intrinsèques spéciales, plutôt que d’inclure des paramètres avec une sémantique spéciale dans la signature de votre fonction de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="09b15-104">System values are retrieved by using special intrinsic functions, rather than including parameters with special semantics in your shader function signature.</span></span> 

## <a name="in-this-section"></a><span data-ttu-id="09b15-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="09b15-105">In this section</span></span>

### <a name="ray-dispatch-system-values"></a><span data-ttu-id="09b15-106">Valeurs système de dispatch de rayon</span><span class="sxs-lookup"><span data-stu-id="09b15-106">Ray dispatch system values</span></span>

| <span data-ttu-id="09b15-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="09b15-107">Topic</span></span> | <span data-ttu-id="09b15-108">Description</span><span class="sxs-lookup"><span data-stu-id="09b15-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="09b15-109">**DispatchRaysIndex**</span><span class="sxs-lookup"><span data-stu-id="09b15-109">**DispatchRaysIndex**</span></span>](dispatchraysindex.md) | <span data-ttu-id="09b15-110">Obtient l’emplacement x et y actuel dans la largeur et la hauteur obtenues avec la valeur système **DispatchRaysDimensions** intrinsèque.</span><span class="sxs-lookup"><span data-stu-id="09b15-110">Gets the current x and y location within the width and height obtained with the **DispatchRaysDimensions** system value intrinsic.</span></span> |
| [<span data-ttu-id="09b15-111">**DispatchRaysDimensions**</span><span class="sxs-lookup"><span data-stu-id="09b15-111">**DispatchRaysDimensions**</span></span>](dispatchraysdimensions.md) | <span data-ttu-id="09b15-112">Valeurs de largeur, de hauteur et de profondeur de la structure **\_ \_ \_ desc des rayons D3D12 Dispatch** spécifiés dans l’appel **DispatchRays** d’origine.</span><span class="sxs-lookup"><span data-stu-id="09b15-112">The width, height and depth values from the **D3D12\_DISPATCH\_RAYS\_DESC** structure specified in the originating **DispatchRays** call.</span></span> |

### <a name="ray-system-values"></a><span data-ttu-id="09b15-113">Valeurs système de rayon</span><span class="sxs-lookup"><span data-stu-id="09b15-113">Ray system values</span></span>

| <span data-ttu-id="09b15-114">Rubrique</span><span class="sxs-lookup"><span data-stu-id="09b15-114">Topic</span></span> | <span data-ttu-id="09b15-115">Description</span><span class="sxs-lookup"><span data-stu-id="09b15-115">Description</span></span> |
|-|-|
| [<span data-ttu-id="09b15-116">**WorldRayOrigin**</span><span class="sxs-lookup"><span data-stu-id="09b15-116">**WorldRayOrigin**</span></span>](worldrayorigin.md) | <span data-ttu-id="09b15-117">Origine de l’espace universel du rayon actuel.</span><span class="sxs-lookup"><span data-stu-id="09b15-117">The world-space origin of the current ray.</span></span> |
| [<span data-ttu-id="09b15-118">**WorldRayDirection**</span><span class="sxs-lookup"><span data-stu-id="09b15-118">**WorldRayDirection**</span></span>](worldraydirection.md) | <span data-ttu-id="09b15-119">Direction de l’espace universel pour le rayon actuel.</span><span class="sxs-lookup"><span data-stu-id="09b15-119">The world-space direction for the current ray.</span></span> |
| [<span data-ttu-id="09b15-120">**RayTMin**</span><span class="sxs-lookup"><span data-stu-id="09b15-120">**RayTMin**</span></span>](raytmin.md) | <span data-ttu-id="09b15-121">Valeur float représentant le point de départ paramétrique actuel pour le rayon.</span><span class="sxs-lookup"><span data-stu-id="09b15-121">A float representing the current parametric starting point for the ray.</span></span> |
| [<span data-ttu-id="09b15-122">**RayTCurrent**</span><span class="sxs-lookup"><span data-stu-id="09b15-122">**RayTCurrent**</span></span>](raytcurrent.md) | <span data-ttu-id="09b15-123">Valeur float représentant le point de terminaison paramétrique actuel pour le rayon.</span><span class="sxs-lookup"><span data-stu-id="09b15-123">A float representing the current parametric ending point for the ray.</span></span>  |
| [<span data-ttu-id="09b15-124">**RayFlags**</span><span class="sxs-lookup"><span data-stu-id="09b15-124">**RayFlags**</span></span>](rayflags.md) | <span data-ttu-id="09b15-125">Entier non signé contenant les indicateurs de **ray_flag** actuels.</span><span class="sxs-lookup"><span data-stu-id="09b15-125">An unsigned integer containing the current **ray_flag** flags.</span></span> |

### <a name="primitiveobject-space-system-values"></a><span data-ttu-id="09b15-126">Valeurs système de l’espace de primitive/objet</span><span class="sxs-lookup"><span data-stu-id="09b15-126">Primitive/object space system values</span></span>

| <span data-ttu-id="09b15-127">Rubrique</span><span class="sxs-lookup"><span data-stu-id="09b15-127">Topic</span></span> | <span data-ttu-id="09b15-128">Description</span><span class="sxs-lookup"><span data-stu-id="09b15-128">Description</span></span> |
|-|-|
| [<span data-ttu-id="09b15-129">**InstanceIndex**</span><span class="sxs-lookup"><span data-stu-id="09b15-129">**InstanceIndex**</span></span>](instanceindex.md) | <span data-ttu-id="09b15-130">Index généré automatiquement de l’instance actuelle dans la structure d’accélération de Raytracing de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="09b15-130">The autogenerated index of the current instance in the top-level raytracing acceleration structure.</span></span> |
| [<span data-ttu-id="09b15-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="09b15-131">**InstanceID**</span></span>](instanceid.md) | <span data-ttu-id="09b15-132">Identificateur fourni par l’utilisateur pour l’instance sur l’instance de la structure d’accélération de niveau inférieur dans la structure de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="09b15-132">The user-provided identifier for the instance on the bottom-level acceleration structure instance within the top-level structure.</span></span> |
| [<span data-ttu-id="09b15-133">**PrimitiveIndex**</span><span class="sxs-lookup"><span data-stu-id="09b15-133">**PrimitiveIndex**</span></span>](primitiveindex.md) | <span data-ttu-id="09b15-134">Index généré automatiquement de la primitive dans la géométrie à l’intérieur de l’instance de la structure d’accélération de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="09b15-134">The autogenerated index of the primitive within the geometry inside the bottom-level acceleration structure instance.</span></span> |
| [<span data-ttu-id="09b15-135">**ObjectRayOrigin**</span><span class="sxs-lookup"><span data-stu-id="09b15-135">**ObjectRayOrigin**</span></span>](objectrayorigin.md) | <span data-ttu-id="09b15-136">Origine de l’espace de l’objet pour le rayon actuel.</span><span class="sxs-lookup"><span data-stu-id="09b15-136">The object-space origin for the current ray.</span></span> |
| [<span data-ttu-id="09b15-137">**ObjectRayDirection**</span><span class="sxs-lookup"><span data-stu-id="09b15-137">**ObjectRayDirection**</span></span>](objectraydirection.md) | <span data-ttu-id="09b15-138">Direction de l’espace de l’objet pour le rayon actuel.</span><span class="sxs-lookup"><span data-stu-id="09b15-138">The object-space direction for the current ray.</span></span> |
| [<span data-ttu-id="09b15-139">**ObjectToWorld3x4**</span><span class="sxs-lookup"><span data-stu-id="09b15-139">**ObjectToWorld3x4**</span></span>](objecttoworld3x4.md) | <span data-ttu-id="09b15-140">Matrice pour la transformation de l’espace objet en espace universel.</span><span class="sxs-lookup"><span data-stu-id="09b15-140">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="09b15-141">**ObjectToWorld4x3**</span><span class="sxs-lookup"><span data-stu-id="09b15-141">**ObjectToWorld4x3**</span></span>](objecttoworld4x3.md) | <span data-ttu-id="09b15-142">Matrice pour la transformation de l’espace objet en espace universel.</span><span class="sxs-lookup"><span data-stu-id="09b15-142">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="09b15-143">**WorldToObject3x4**</span><span class="sxs-lookup"><span data-stu-id="09b15-143">**WorldToObject3x4**</span></span>](worldtoobject3x4.md) | <span data-ttu-id="09b15-144">Matrice pour la transformation de l’espace universel à l’espace d’objet</span><span class="sxs-lookup"><span data-stu-id="09b15-144">A matrix for transforming from world-space to object-space</span></span> |
| [<span data-ttu-id="09b15-145">**WorldToObject4x3**</span><span class="sxs-lookup"><span data-stu-id="09b15-145">**WorldToObject4x3**</span></span>](worldtoobject4x3.md) | <span data-ttu-id="09b15-146">Matrice pour la transformation de l’espace universel à l’espace d’objet</span><span class="sxs-lookup"><span data-stu-id="09b15-146">A matrix for transforming from world-space to object-space</span></span> |
### <a name="hit-specific-system-values"></a><span data-ttu-id="09b15-147">Valeurs système spécifiques à l’accès</span><span class="sxs-lookup"><span data-stu-id="09b15-147">Hit-specific system values</span></span>

| <span data-ttu-id="09b15-148">Rubrique</span><span class="sxs-lookup"><span data-stu-id="09b15-148">Topic</span></span> | <span data-ttu-id="09b15-149">Description</span><span class="sxs-lookup"><span data-stu-id="09b15-149">Description</span></span> |
|-|-|
| [<span data-ttu-id="09b15-150">**HitKind**</span><span class="sxs-lookup"><span data-stu-id="09b15-150">**HitKind**</span></span>](hitkind.md) | <span data-ttu-id="09b15-151">Retourne la valeur passée comme paramètre **HitKind** à [**ReportHit**](reporthit-function.md).</span><span class="sxs-lookup"><span data-stu-id="09b15-151">Returns the value passed as the **HitKind** parameter to [**ReportHit**](reporthit-function.md).</span></span> |

## <a name="related-topics"></a><span data-ttu-id="09b15-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09b15-152">Related topics</span></span>

* [<span data-ttu-id="09b15-153">Référence principale</span><span class="sxs-lookup"><span data-stu-id="09b15-153">Core Reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="09b15-154">Référence de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="09b15-154">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
