---
title: Structure des attributs d’intersection
description: Structure déclarée en HLSL pour représenter des attributs d’accès pour l’intersection de triangle de fonction fixe ou le cadre englobant aligné sur l’axe pour l’intersection de la primitive procédurale.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f1dd8fee7371f81dd538b6ea6622f22e3bfd3d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "106531447"
---
# <a name="intersection-attributes-structure"></a><span data-ttu-id="15635-103">Structure des attributs d’intersection</span><span class="sxs-lookup"><span data-stu-id="15635-103">Intersection attributes structure</span></span> 

<span data-ttu-id="15635-104">Structure déclarée en HLSL pour représenter des attributs d’accès pour l’intersection de triangle de fonction fixe ou le cadre englobant aligné sur l’axe pour l’intersection de la primitive procédurale.</span><span class="sxs-lookup"><span data-stu-id="15635-104">A structure declared in HLSL to represent hit attributes for fixed-function triangle intersection or axis-aligned bounding box for procedural primitive intersection.</span></span>

## <a name="fixed-function-triangle-intersection"></a><span data-ttu-id="15635-105">Intersection de triangle de fonction fixe</span><span class="sxs-lookup"><span data-stu-id="15635-105">Fixed-function triangle intersection</span></span>

<span data-ttu-id="15635-106">La structure suivante est déclarée en HLSL pour représenter des attributs d’accès pour l’intersection de triangle de fonction fixe :</span><span class="sxs-lookup"><span data-stu-id="15635-106">The following structure is declared in HLSL to represent hit attributes for fixed-function triangle intersection:</span></span>


```
struct BuiltInTriangleIntersectionAttributes
{
    float2 barycentrics;
};
```

<span data-ttu-id="15635-107">[Les](any-hit-shader.md) nuanceurs atteints et les nuanceurs [atteints les plus proches](closest-hit-shader.md) , appelés à l’aide d’une intersection de triangle à fonction fixe, doivent utiliser cette structure pour les attributs d’accès.</span><span class="sxs-lookup"><span data-stu-id="15635-107">[Any hit](any-hit-shader.md) and [closest hit](closest-hit-shader.md) shaders invoked using fixed-function triangle intersection must use this structure for hit attributes.</span></span> <span data-ttu-id="15635-108">Les attributs donnés a0, a1 et a2 pour les 3 vertex d’un triangle, barycentrics. x est le poids de a1 et barycentrics. y est le poids de a2.</span><span class="sxs-lookup"><span data-stu-id="15635-108">Given attributes a0, a1 and a2 for the 3 vertices of a triangle, barycentrics.x is the weight for a1 and barycentrics.y is the weight for a2.</span></span>  <span data-ttu-id="15635-109">Par exemple, l’application peut interpoler en procédant comme suit : a = a0 + barycentrics. x \* (a1-a0) + barycentrics. y \* (a2 – a0).</span><span class="sxs-lookup"><span data-stu-id="15635-109">For example, the app can interpolate by doing:  a = a0 + barycentrics.x \* (a1-a0) + barycentrics.y\* (a2 – a0).</span></span>

## <a name="axis-aligned-bounding-box-for-procedural-primitive-intersection"></a><span data-ttu-id="15635-110">Cadre englobant aligné sur l’axe pour l’intersection de la primitive procédurale</span><span class="sxs-lookup"><span data-stu-id="15635-110">Axis-aligned bounding box for procedural primitive intersection</span></span>

<span data-ttu-id="15635-111">Lorsque les zones englobantes alignées sur l’axe sont utilisées pour l’intersection avec les primitives procédurales, un nuanceur d’intersection est déclenché.</span><span class="sxs-lookup"><span data-stu-id="15635-111">When axis-aligned bounding boxes are used for intersection with procedural primitives, an intersection shader is triggered.</span></span>  <span data-ttu-id="15635-112">Ce nuanceur fournit une structure d’attribut d’intersection définie par l’utilisateur à l’appel [**ReportHit**](reporthit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="15635-112">That shader provides a user-defined intersection attribute structure to the [**ReportHit**](reporthit-function.md) call.</span></span>  <span data-ttu-id="15635-113">Les nuanceurs d’atteinte et les nuanceurs atteints les plus proches dans le même groupe d’accès avec ce nuanceur d’intersection doivent utiliser la même structure pour les attributs de positionnement, même si les attributs ne sont pas référencés.</span><span class="sxs-lookup"><span data-stu-id="15635-113">The any hit and closest hit shaders bound in the same hit group with this intersection shader must use the same structure for hit attributes, even if the attributes are not referenced.</span></span>  <span data-ttu-id="15635-114">La taille maximale de la structure des attributs est de 32 octets, définie comme **\_ \_ \_ taille d’attribut D3D12 RAYTRACING Max \_ \_ en \_ octets**.</span><span class="sxs-lookup"><span data-stu-id="15635-114">The maximum attribute structure size is 32 bytes, defined as **D3D12\_RAYTRACING\_MAX\_ATTRIBUTE\_SIZE\_IN\_BYTES**.</span></span>


