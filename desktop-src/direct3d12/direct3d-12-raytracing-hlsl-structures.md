---
title: Structures HLSL Raytracing (Direct3D 12)
description: Les structures HLSL suivantes prennent en charge le pipeline Direct3D 12 Raytracing.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c48ad6bac76e200587ec76d42dfa9c86b23cd23
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "106510659"
---
# <a name="raytracing-hlsl-structures-direct3d-12"></a><span data-ttu-id="42812-103">Structures HLSL Raytracing (Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="42812-103">Raytracing HLSL structures (Direct3D 12)</span></span>

<span data-ttu-id="42812-104">Les structures HLSL suivantes prennent en charge le pipeline Direct3D 12 Raytracing.</span><span class="sxs-lookup"><span data-stu-id="42812-104">The following HLSL structures support the Direct3D 12 raytracing pipeline.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="42812-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="42812-105">In this section</span></span>



| <span data-ttu-id="42812-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="42812-106">Topic</span></span>                                                                                                       | <span data-ttu-id="42812-107">Description</span><span class="sxs-lookup"><span data-stu-id="42812-107">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42812-108">**Structure des paramètres d’appel**</span><span class="sxs-lookup"><span data-stu-id="42812-108">**Call Parameter Structure**</span></span>](call-parameter-structure.md)<br/>                              | <span data-ttu-id="42812-109">Une structure définie par l’utilisateur fournie en tant qu’argument INOUT à un appel CallShader, et en tant que paramètre INOUT pour le nuanceur pouvant être appelé.</span><span class="sxs-lookup"><span data-stu-id="42812-109">A user-defined structure provided as an inout argument to a CallShader call, and as an inout parameter for the callable shader.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="42812-110">**Structure des attributs d’intersection**</span><span class="sxs-lookup"><span data-stu-id="42812-110">**Intersection Attributes Structure**</span></span>](intersection-attributes.md)<br/>                              | <span data-ttu-id="42812-111">Structure définie par l’utilisateur qui est fournie en tant qu’argument INOUT dans un appel [**TraceRay**](traceray-function.md) , et en tant que paramètre INOUT dans les types de nuanceur qui peuvent accéder à la charge utile de rayon.</span><span class="sxs-lookup"><span data-stu-id="42812-111">A user-defined structure that is provided as an inout argument in a [**TraceRay**](traceray-function.md) call, and as an inout parameter in the shader types that may access the ray payload.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="42812-112">**Structure de charge utile de rayon**</span><span class="sxs-lookup"><span data-stu-id="42812-112">**Ray Payload Structure**</span></span>](ray-payload.md)<br/>                              | <span data-ttu-id="42812-113">Structure définie par l’utilisateur qui est fournie en tant qu’argument INOUT dans un appel [**TraceRay**](traceray-function.md) , et en tant que paramètre INOUT dans les types de nuanceur qui peuvent accéder à la charge utile de rayon.</span><span class="sxs-lookup"><span data-stu-id="42812-113">A user-defined structure that is provided as an inout argument in a [**TraceRay**](traceray-function.md) call, and as an inout parameter in the shader types that may access the ray payload.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="42812-114">**Structure RayDesc**</span><span class="sxs-lookup"><span data-stu-id="42812-114">**RayDesc Structure**</span></span>](raydesc.md)<br/>                              | <span data-ttu-id="42812-115">Indicateurs passés à la fonction [**TraceRay**](traceray-function.md) pour remplacer la transparence, l’élimination et le comportement précoce.</span><span class="sxs-lookup"><span data-stu-id="42812-115">Flags passed to the [**TraceRay**](traceray-function.md) function to override transparency, culling, and early-out behavior.</span></span><br/>                                                                                                                                                                                                                                              |





 

## <a name="related-topics"></a><span data-ttu-id="42812-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="42812-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42812-117">Référence principale</span><span class="sxs-lookup"><span data-stu-id="42812-117">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="42812-118">Référence de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="42812-118">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





