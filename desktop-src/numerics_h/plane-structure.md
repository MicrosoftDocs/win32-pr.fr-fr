---
title: structure du plan (Windowsnumerics. h)
description: Cette structure représente un plan à l’aide d’une valeur normale de vecteur 3D et d’une distance.
ms.assetid: 3C5A5EA0-8A51-4F9B-A84A-0C8E726CE3FD
keywords:
- structure du plan
topic_type:
- apiref
api_name:
- plane structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d870e2769121b4aec542235081011406e439d579
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526450"
---
# <a name="plane-structure"></a><span data-ttu-id="88b79-104">structure du plan</span><span class="sxs-lookup"><span data-stu-id="88b79-104">plane structure</span></span>

<span data-ttu-id="88b79-105">Cette structure représente un plan à l’aide d’une valeur normale de vecteur 3D et d’une distance.</span><span class="sxs-lookup"><span data-stu-id="88b79-105">This structure represents a plane using a 3D vector normal and a distance value.</span></span>

<span data-ttu-id="88b79-106">Ce type est disponible uniquement en C++.</span><span class="sxs-lookup"><span data-stu-id="88b79-106">This type is available only in C++.</span></span> <span data-ttu-id="88b79-107">Son équivalent .NET est [System. Numerics. plan](/dotnet/api/system.numerics.plane?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="88b79-107">Its .NET equivalent is [System.Numerics.Plane](/dotnet/api/system.numerics.plane?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="88b79-108">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="88b79-108">Constructors</span></span>

| <span data-ttu-id="88b79-109">Nom</span><span class="sxs-lookup"><span data-stu-id="88b79-109">Name</span></span> | <span data-ttu-id="88b79-110">Description</span><span class="sxs-lookup"><span data-stu-id="88b79-110">Description</span></span> |
|-|-|
| `plane()` | <span data-ttu-id="88b79-111">Crée un plan non initialisé.</span><span class="sxs-lookup"><span data-stu-id="88b79-111">Creates an uninitialized plane.</span></span> |
| `plane(float x, float y, float z, float d)` | <span data-ttu-id="88b79-112">Crée un plan avec les valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="88b79-112">Creates a plane with the specified values.</span></span> |
| `plane(float3 normal, float d)` | <span data-ttu-id="88b79-113">Crée un plan à partir d’un float3 et d’une distance.</span><span class="sxs-lookup"><span data-stu-id="88b79-113">Creates a plane from a float3 and a distance.</span></span> |
| `explicit plane(float4 value)` | <span data-ttu-id="88b79-114">Crée un plan à partir d’un float4.</span><span class="sxs-lookup"><span data-stu-id="88b79-114">Creates a plane from a float4.</span></span> |
| `plane(Microsoft::?Graphics::?Canvas::?Numerics::?Plane const& value)` | <span data-ttu-id="88b79-115">Convertit un **Microsoft. Graphics. Canvas. Numerics. plan** en plan.</span><span class="sxs-lookup"><span data-stu-id="88b79-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Plane** to a plane.</span></span> |

## <a name="functions"></a><span data-ttu-id="88b79-116">Fonctions</span><span class="sxs-lookup"><span data-stu-id="88b79-116">Functions</span></span>

| <span data-ttu-id="88b79-117">Nom</span><span class="sxs-lookup"><span data-stu-id="88b79-117">Name</span></span> | <span data-ttu-id="88b79-118">Description</span><span class="sxs-lookup"><span data-stu-id="88b79-118">Description</span></span> |
|-|-|
| `plane make_plane_from_vertices(float3 const& point1, float3 const& point2, float3 const& point3)` | <span data-ttu-id="88b79-119">Crée un plan à partir d’un ensemble de trois positions de vertex, qui doivent toutes être différentes et ne pas être en ligne droite.</span><span class="sxs-lookup"><span data-stu-id="88b79-119">Creates a plane from a set of three vertex positions, which must all be different and not in a straight line.</span></span> |
| `plane normalize(plane const& value)` | <span data-ttu-id="88b79-120">Modifie les coefficients du vecteur normal d’un plan pour l’ajuster à la longueur de l’unité.</span><span class="sxs-lookup"><span data-stu-id="88b79-120">Changes the coefficients of the normal vector of a plane to make it of unit length.</span></span> |
| `plane transform(plane const& plane, float4x4 const& matrix)` | <span data-ttu-id="88b79-121">Transforme un plan normalisé par une matrice.</span><span class="sxs-lookup"><span data-stu-id="88b79-121">Transforms a normalized plane by a matrix.</span></span> |
| `plane transform(plane const& plane, quaternion const& rotation)` | <span data-ttu-id="88b79-122">Transforme un plan normalisé par une rotation de Quaternion.</span><span class="sxs-lookup"><span data-stu-id="88b79-122">Transforms a normalized plane by a quaternion rotation.</span></span> |
| `float dot(plane const& plane, float4 const& value)` | <span data-ttu-id="88b79-123">Calcule le produit scalaire d’un plan à l’aide d’un vecteur.</span><span class="sxs-lookup"><span data-stu-id="88b79-123">Calculates the dot product of a plane with a vector.</span></span> |
| `float dot_coordinate(plane const& plane, float3 const& value)` | <span data-ttu-id="88b79-124">Calcule le produit scalaire d’un plan avec une coordonnée float3.</span><span class="sxs-lookup"><span data-stu-id="88b79-124">Calculates the dot product of a plane with a float3 coordinate.</span></span> <span data-ttu-id="88b79-125">Contrairement \_ au point normal, ce calcul comprend la valeur du plan d.</span><span class="sxs-lookup"><span data-stu-id="88b79-125">Unlike dot\_normal, this computation includes the plane d value.</span></span> |
| `float dot_normal(plane const& plane, float3 const& value)` | <span data-ttu-id="88b79-126">Calcule le produit scalaire d’un plan avec un float3 normal.</span><span class="sxs-lookup"><span data-stu-id="88b79-126">Calculates the dot product of a plane with a float3 normal.</span></span> <span data-ttu-id="88b79-127">Contrairement à \_ la coordonnée de points, ce calcul ignore la valeur du plan d.</span><span class="sxs-lookup"><span data-stu-id="88b79-127">Unlike dot\_coordinate, this computation ignores the plane d value.</span></span> |

## <a name="operators"></a><span data-ttu-id="88b79-128">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="88b79-128">Operators</span></span>

| <span data-ttu-id="88b79-129">Nom</span><span class="sxs-lookup"><span data-stu-id="88b79-129">Name</span></span> | <span data-ttu-id="88b79-130">Description</span><span class="sxs-lookup"><span data-stu-id="88b79-130">Description</span></span> |
|-|-|
| `bool operator== (plane const& value1, plane const& value2)` | <span data-ttu-id="88b79-131">Détermine si deux instances de plan sont égales.</span><span class="sxs-lookup"><span data-stu-id="88b79-131">Determines whether two instances of plane are equal.</span></span> |
| `bool operator!= (plane const& value1, plane const& value2)` | <span data-ttu-id="88b79-132">Détermine si deux instances de plan ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="88b79-132">Determines whether two instances of plane are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Plane() const` | <span data-ttu-id="88b79-133">Convertit un plan en un **Microsoft. Graphics. canevas. Numerics. plan**.</span><span class="sxs-lookup"><span data-stu-id="88b79-133">Converts a plane to a **Microsoft.Graphics.Canvas.Numerics.Plane**.</span></span> |

## <a name="fields"></a><span data-ttu-id="88b79-134">Champs</span><span class="sxs-lookup"><span data-stu-id="88b79-134">Fields</span></span>

| <span data-ttu-id="88b79-135">Nom</span><span class="sxs-lookup"><span data-stu-id="88b79-135">Name</span></span> | <span data-ttu-id="88b79-136">Description</span><span class="sxs-lookup"><span data-stu-id="88b79-136">Description</span></span> |
|-|-|
| `float3 normal` | <span data-ttu-id="88b79-137">Vecteur normal du plan.</span><span class="sxs-lookup"><span data-stu-id="88b79-137">Normal vector of the plane.</span></span> |
| `float d` | <span data-ttu-id="88b79-138">Distance du plan le long de sa normale par rapport à l’origine.</span><span class="sxs-lookup"><span data-stu-id="88b79-138">Distance of the plane along its normal from the origin.</span></span> |

## <a name="requirements"></a><span data-ttu-id="88b79-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88b79-139">Requirements</span></span>

| <span data-ttu-id="88b79-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88b79-140">Requirement</span></span> | <span data-ttu-id="88b79-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="88b79-141">Value</span></span> |
|-|-|
| <span data-ttu-id="88b79-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="88b79-142">Namespace</span></span> | <span data-ttu-id="88b79-143">Windows :: Foundation :: Numerics</span><span class="sxs-lookup"><span data-stu-id="88b79-143">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="88b79-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="88b79-144">Header</span></span> | <dl> <span data-ttu-id="88b79-145"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="88b79-145"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="88b79-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88b79-146">See also</span></span>

[<span data-ttu-id="88b79-147">API windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="88b79-147">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
