---
description: Un nuanceur qui est appelé quand les intersections de rayon ne sont pas opaques.
ms.assetid: ''
title: Tout nuanceur de correspondance
ms.date: 05/31/2018
ms.topic: reference
ms.localizationpriority: low
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: aad2f8b94f6ea53d500d285cac3555f5ff8b95f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106522659"
---
# <a name="any-hit-shader"></a><span data-ttu-id="7e69b-103">Tout nuanceur de correspondance</span><span class="sxs-lookup"><span data-stu-id="7e69b-103">Any Hit Shader</span></span>

<span data-ttu-id="7e69b-104">Un nuanceur qui est appelé quand les intersections de rayon ne sont pas opaques.</span><span class="sxs-lookup"><span data-stu-id="7e69b-104">A shader that is invoked when ray intersections are not opaque.</span></span> 

<span data-ttu-id="7e69b-105">Les nuanceurs d’accès doivent déclarer un paramètre de charge utile suivi d’un paramètre d’attributs.</span><span class="sxs-lookup"><span data-stu-id="7e69b-105">Any hit shaders must declare a payload parameter followed by an attributes parameter.</span></span> <span data-ttu-id="7e69b-106">Chacun de ces paramètres doit être un type de structure défini par l’utilisateur correspondant aux types utilisés pour [**TraceRay**](traceray-function.md) et [**ReportHit**](reporthit-function.md) respectivement, ou la [**structure d’attributs d’intersection**](intersection-attributes.md) quand l’intersection de triangle de fonction fixe est utilisée.</span><span class="sxs-lookup"><span data-stu-id="7e69b-106">Each of these parameters must be a user-defined structure type matching types used for [**TraceRay**](traceray-function.md) and [**ReportHit**](reporthit-function.md) respectively, or the [**Intersection Attributes Structure**](intersection-attributes.md) when fixed function triangle intersection is used.</span></span>

<span data-ttu-id="7e69b-107">Les nuanceurs d’accès peuvent effectuer les types d’opérations suivants :</span><span class="sxs-lookup"><span data-stu-id="7e69b-107">Any hit shaders may perform the following kinds of operations:</span></span>

*   <span data-ttu-id="7e69b-108">Lire et modifier la charge utile Ray : (INOUT payload_t rayPayload)</span><span class="sxs-lookup"><span data-stu-id="7e69b-108">Read and modify the ray payload: (inout payload_t rayPayload)</span></span>
*   <span data-ttu-id="7e69b-109">Lire les attributs d’intersection : (dans attr_t attributs)</span><span class="sxs-lookup"><span data-stu-id="7e69b-109">Read the intersection attributes: (in attr_t attributes)</span></span>
*   <span data-ttu-id="7e69b-110">Appelez [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), qui accepte l’accès actuel, met fin au [nuanceur de correspondance](any-hit-shader.md), termine le [nuanceur d’intersection](intersection-shader.md) s’il y en a un, puis exécute le [nuanceur de correspondance](closest-hit-shader.md) le plus proche sur le point le plus proche, jusqu’à présent, s’il est actif.</span><span class="sxs-lookup"><span data-stu-id="7e69b-110">Call [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), which accepts the current hit, ends the [any hit shader](any-hit-shader.md), ends the [intersection shader](intersection-shader.md) if one is present, and executes the [closest hit shader](closest-hit-shader.md) on the closest hit so far if it is active.</span></span>
*   <span data-ttu-id="7e69b-111">Appelez [**IgnoreHit**](ignorehit-function.md), qui met fin au nuanceur de correspondance et indique au système de continuer à rechercher les résultats, y compris le renvoi du contrôle à un nuanceur d’intersection, s’il est en cours d’exécution, en renvoyant false à partir du site d’appel [**ReportHit**](reporthit-function.md)\*.</span><span class="sxs-lookup"><span data-stu-id="7e69b-111">Call [**IgnoreHit**](ignorehit-function.md), which ends the any hit shader and tells the system to continue searching for hits, including returning control to an intersection shader, if it is currently executing, returning false from the [**ReportHit**](reporthit-function.md)\* call site.</span></span> 
*   <span data-ttu-id="7e69b-112">Retourne sans appeler l’une de ces fonctions intrinsèques, qui accepte l’accès actuel et indique au système de continuer à rechercher les correspondances, y compris le retour du contrôle au nuanceur d’intersection le cas échéant, en retournant la valeur true sur le site d’appel [**ReportHit**](reporthit-function.md) pour indiquer que l’accès a été accepté.</span><span class="sxs-lookup"><span data-stu-id="7e69b-112">Return without calling either of these intrinsics, which accepts the current hit and tells the system to continue searching for hits, including returning control to the intersection shader if there is one, returning true at the [**ReportHit**](reporthit-function.md) call site to indicate that the hit was accepted.</span></span>

<span data-ttu-id="7e69b-113">Même si un appel de nuanceur atteint se termine par [**IgnoreHit**](ignorehit-function.md) ou [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), toutes les modifications apportées à la charge utile de rayon jusqu’à présent doivent toujours être conservées.</span><span class="sxs-lookup"><span data-stu-id="7e69b-113">Even if an any hit shader invocation is ended by [**IgnoreHit**](ignorehit-function.md) or [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), any modifications made to the ray payload so far must still be retained.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="7e69b-114">Attribut de type Shader</span><span class="sxs-lookup"><span data-stu-id="7e69b-114">Shader Type attribute</span></span>

```
[shader("anyhit")]
```

## <a name="example"></a><span data-ttu-id="7e69b-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="7e69b-115">Example</span></span>

```
[shader("anyhit")]
void anyhit_main( inout MyPayload payload, in MyAttributes attr )
{
    float3 hitLocation = ObjectRayOrigin() + ObjectRayDirection() * RayTCurrent();
    float alpha = computeAlpha(hitLocation, attr, ...);

    // Processing shadow and only care if a hit is registered?
    if (TerminateShadowRay(alpha))
        AcceptHitAndEndSearch(); // aborts function

    // Save alpha contribution and ignoring hit?
    if (SaveAndIgnore(payload, RayTCurrent(), alpha, attr, ...))
        IgnoreHit(); // aborts function

    // do something else
    // return to accept and update closest hit
}
```
