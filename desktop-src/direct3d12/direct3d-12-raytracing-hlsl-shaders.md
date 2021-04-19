---
title: Nuanceurs HLSL Direct3D 12 Raytracing
description: Les nuanceurs HLSL suivants prennent en charge le pipeline Direct3D 12 Raytracing.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1dd545532208095781f6fbca25480a6dbfd31e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106512769"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a><span data-ttu-id="bf8e2-103">Nuanceurs HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="bf8e2-103">Direct3D 12 Raytracing HLSL Shaders</span></span>

<span data-ttu-id="bf8e2-104">Les nuanceurs HLSL suivants prennent en charge le pipeline Direct3D 12 Raytracing.</span><span class="sxs-lookup"><span data-stu-id="bf8e2-104">The following HLSL shaders support the Direct3D 12 raytracing pipeline.</span></span> <span data-ttu-id="bf8e2-105">Ces nuanceurs sont des fonctions compilées dans une bibliothèque, avec lib_6_3 de modèle cible et identifiées par un attribut *[Shader ("shadertype")]* sur la fonction de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="bf8e2-105">These shaders are functions compiled into a library, with target model lib_6_3, and identified by an attribute *[shader("shadertype")]* on the shader function.</span></span> <span data-ttu-id="bf8e2-106">Consultez valeurs **intrinsèques** et **valeurs système** pour voir ce qui est autorisé pour chaque type de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="bf8e2-106">See **Intrinsics** and **System Values** to see what is allowed for each shader type.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bf8e2-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="bf8e2-107">In this section</span></span>



| <span data-ttu-id="bf8e2-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="bf8e2-108">Topic</span></span>                                                                                                       | <span data-ttu-id="bf8e2-109">Description</span><span class="sxs-lookup"><span data-stu-id="bf8e2-109">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf8e2-110">**Tout nuanceur de correspondance**</span><span class="sxs-lookup"><span data-stu-id="bf8e2-110">**Any Hit Shader**</span></span>](any-hit-shader.md)<br/>                              | <span data-ttu-id="bf8e2-111">Un nuanceur qui est appelé quand les intersections de rayon ne sont pas opaques.</span><span class="sxs-lookup"><span data-stu-id="bf8e2-111">A shader that is invoked when ray intersections are not opaque.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="bf8e2-112">**Nuanceur pouvant être appelé**</span><span class="sxs-lookup"><span data-stu-id="bf8e2-112">**Callable Shader**</span></span>](callable-shader.md)<br/>                              | <span data-ttu-id="bf8e2-113">Un nuanceur qui est appelé à partir d’un autre nuanceur avec l’intrinsèque **CallShader** .</span><span class="sxs-lookup"><span data-stu-id="bf8e2-113">A shader that is invoked from another shader with the **CallShader** intrinsic.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="bf8e2-114">**Nuanceur de correspondance le plus proche**</span><span class="sxs-lookup"><span data-stu-id="bf8e2-114">**Closest Hit Shader**</span></span>](closest-hit-shader.md)<br/>                              | <span data-ttu-id="bf8e2-115">Nuanceur appelé lorsqu’il est activé et que l’accès le plus proche a été déterminé ou que la recherche d’intersection de rayon s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="bf8e2-115">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="bf8e2-116">**Nuanceur d’intersection**</span><span class="sxs-lookup"><span data-stu-id="bf8e2-116">**Intersection Shader**</span></span>](intersection-shader.md)<br/>                              | <span data-ttu-id="bf8e2-117">Nuanceur utilisé pour implémenter des primitives d’intersection personnalisées pour les rayons qui croisent un volume englobant associé (cadre englobant).</span><span class="sxs-lookup"><span data-stu-id="bf8e2-117">A shader that is used to implement custom intersection primitives for rays intersecting an associated bounding volume (bounding box).</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="bf8e2-118">**Nuanceur manque**</span><span class="sxs-lookup"><span data-stu-id="bf8e2-118">**Miss Shader**</span></span>](miss-shader.md)<br/>                              | <span data-ttu-id="bf8e2-119">Nuanceur qui est appelé quand aucune intersection de rayon n’est trouvée ou acceptée.</span><span class="sxs-lookup"><span data-stu-id="bf8e2-119">A shader that is invoked when no ray intersections are found or accepted.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="bf8e2-120">**Nuanceur de création de rayon**</span><span class="sxs-lookup"><span data-stu-id="bf8e2-120">**Ray Generation Shader**</span></span>](ray-generation-shader.md)<br/>                              | <span data-ttu-id="bf8e2-121">Nuanceur qui appelle [**TraceRay**](traceray-function.md) pour générer des rayons.</span><span class="sxs-lookup"><span data-stu-id="bf8e2-121">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span><br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a><span data-ttu-id="bf8e2-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bf8e2-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf8e2-123">Référence principale</span><span class="sxs-lookup"><span data-stu-id="bf8e2-123">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="bf8e2-124">Référence de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="bf8e2-124">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





