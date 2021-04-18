---
title: float3, structure (Windowsnumerics. h)
description: Vecteur avec trois composants.
ms.assetid: CAA10ADA-C5A8-4B75-A0A9-5C5B3FDD9A07
keywords:
- float3, structure
topic_type:
- apiref
api_name:
- float3 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ae524205c900c63438a50094dcd551a4903632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526451"
---
# <a name="float3-structure"></a><span data-ttu-id="6d463-104">float3, structure</span><span class="sxs-lookup"><span data-stu-id="6d463-104">float3 structure</span></span>

<span data-ttu-id="6d463-105">Vecteur avec trois composants.</span><span class="sxs-lookup"><span data-stu-id="6d463-105">A vector with three components.</span></span>

<span data-ttu-id="6d463-106">Ce type est disponible uniquement en C++.</span><span class="sxs-lookup"><span data-stu-id="6d463-106">This type is available only in C++.</span></span> <span data-ttu-id="6d463-107">Son équivalent .NET est [System. Numerics. Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="6d463-107">Its .NET equivalent is [System.Numerics.Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="6d463-108">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="6d463-108">Constructors</span></span>

| <span data-ttu-id="6d463-109">Nom</span><span class="sxs-lookup"><span data-stu-id="6d463-109">Name</span></span> | <span data-ttu-id="6d463-110">Description</span><span class="sxs-lookup"><span data-stu-id="6d463-110">Description</span></span> |
|-|-|
| `float3()` | <span data-ttu-id="6d463-111">Crée un float3 non initialisé.</span><span class="sxs-lookup"><span data-stu-id="6d463-111">Creates an uninitialized float3.</span></span> |
| `float3(float x, float y, float z)` | <span data-ttu-id="6d463-112">Crée un float3 avec les valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="6d463-112">Creates a float3 with the specified values.</span></span> |
| `float3(float2 value, float z)` | <span data-ttu-id="6d463-113">Crée un float3 avec x et y copié à partir d’un float2 plus la valeur z spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6d463-113">Creates a float3 with x and y copied from a float2 plus the specified z value.</span></span> |
| `explicit float3(float value)` | <span data-ttu-id="6d463-114">Crée un float3 avec tous les composants définis sur la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6d463-114">Creates a float3 with all components set to the specified value.</span></span> |
| `float3(Microsoft::Graphics::Canvas::Numerics::Vector3 const& value)` | <span data-ttu-id="6d463-115">Convertit un **Microsoft. Graphics. canevas. Numerics. Vector3** en float3.</span><span class="sxs-lookup"><span data-stu-id="6d463-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector3** to a float3.</span></span> |

## <a name="functions"></a><span data-ttu-id="6d463-116">Fonctions</span><span class="sxs-lookup"><span data-stu-id="6d463-116">Functions</span></span>

| <span data-ttu-id="6d463-117">Nom</span><span class="sxs-lookup"><span data-stu-id="6d463-117">Name</span></span> | <span data-ttu-id="6d463-118">Description</span><span class="sxs-lookup"><span data-stu-id="6d463-118">Description</span></span> |
|-|-|
| `float length(float3 const& value)` | <span data-ttu-id="6d463-119">Calcule la longueur, ou distance euclidienne, du vecteur.</span><span class="sxs-lookup"><span data-stu-id="6d463-119">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float3 const& value)` | <span data-ttu-id="6d463-120">Calcule la longueur, ou distance euclidienne, du vecteur carré.</span><span class="sxs-lookup"><span data-stu-id="6d463-120">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float3 const& value1, float3 const& value2)` | <span data-ttu-id="6d463-121">Calcule la distance euclidienne entre deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="6d463-121">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float3 const& value1, float3 const& value2)` | <span data-ttu-id="6d463-122">Calcule la distance euclidienne entre deux vecteurs carrés.</span><span class="sxs-lookup"><span data-stu-id="6d463-122">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float3 const& vector1, float3 const& vector2)` | <span data-ttu-id="6d463-123">Calcule le produit scalaire de deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="6d463-123">Calculates the dot product of two vectors.</span></span> |
| `float3 normalize(float3 const& value)` | <span data-ttu-id="6d463-124">Crée un vecteur d’unité à partir du vecteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="6d463-124">Creates a unit vector from the specified vector.</span></span> |
| `float3 cross(float3 const& vector1, float3 const& vector2)` | <span data-ttu-id="6d463-125">Calcule le produit croisé de deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="6d463-125">Calculates the cross product of two vectors.</span></span> |
| `float3 reflect(float3 const& vector, float3 const& normal)` | <span data-ttu-id="6d463-126">Détermine le vecteur réfléchissant du vecteur donné et normal.</span><span class="sxs-lookup"><span data-stu-id="6d463-126">Determines the reflect vector of the given vector and normal.</span></span> |
| `float3 min(float3 const& value1, float3 const& value2)` | <span data-ttu-id="6d463-127">Retourne un vecteur qui contient la valeur la plus faible de chaque paire de composants correspondante.</span><span class="sxs-lookup"><span data-stu-id="6d463-127">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float3 max(float3 const& value1, float3 const& value2)` | <span data-ttu-id="6d463-128">Retourne un vecteur qui contient la valeur la plus élevée de chaque paire de composants correspondante.</span><span class="sxs-lookup"><span data-stu-id="6d463-128">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float3 clamp(float3 const& value1, float3 const& min, float3 const& max)` | <span data-ttu-id="6d463-129">Restreint une valeur à une plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6d463-129">Restricts a value to be within a specified range.</span></span> |
| `float3 lerp(float3 const& value1, float3 const& value2, float amount)` | <span data-ttu-id="6d463-130">Effectue une interpolation linéaire entre deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="6d463-130">Performs a linear interpolation between two vectors.</span></span> |
| `float3 transform(float3 const& position, float4x4 const& matrix)` | <span data-ttu-id="6d463-131">Transforme le vecteur (x, y, z, 1) par la matrice spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6d463-131">Transforms the vector (x, y, z, 1) by the specified matrix.</span></span> |
| `float3 transform_normal(float3 const& normal, float4x4 const& matrix)` | <span data-ttu-id="6d463-132">Transforme le vecteur normal (x, y, z, 0) par la matrice spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6d463-132">Transforms the normal vector (x, y, z, 0) by the specified matrix.</span></span> |
| `float3 transform(float3 const& value, quaternion const& rotation)` | <span data-ttu-id="6d463-133">Transforme un float3 par le Quaternion donné.</span><span class="sxs-lookup"><span data-stu-id="6d463-133">Transforms a float3 by the given quaternion.</span></span> |

## <a name="methods"></a><span data-ttu-id="6d463-134">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6d463-134">Methods</span></span>

| <span data-ttu-id="6d463-135">Nom</span><span class="sxs-lookup"><span data-stu-id="6d463-135">Name</span></span> | <span data-ttu-id="6d463-136">Description</span><span class="sxs-lookup"><span data-stu-id="6d463-136">Description</span></span> |
|-|-|
| `static float3 zero()` | <span data-ttu-id="6d463-137">Retourne un float3 avec tous ses composants définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="6d463-137">Returns a float3 with all of its components set to zero.</span></span> |
| `static float3 one()` | <span data-ttu-id="6d463-138">Retourne un float3 avec tous ses composants définis sur un.</span><span class="sxs-lookup"><span data-stu-id="6d463-138">Returns a float3 with all of its components set to one.</span></span> |
| `static float3 unit_x()` | <span data-ttu-id="6d463-139">Retourne float3 (1, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="6d463-139">Returns the float3 (1, 0, 0).</span></span> |
| `static float3 unit_y()` | <span data-ttu-id="6d463-140">Retourne float3 (0, 1, 0).</span><span class="sxs-lookup"><span data-stu-id="6d463-140">Returns the float3 (0, 1, 0).</span></span> |
| `static float3 unit_z()` | <span data-ttu-id="6d463-141">Retourne float3 (0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="6d463-141">Returns the float3 (0, 0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="6d463-142">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="6d463-142">Operators</span></span>

| <span data-ttu-id="6d463-143">Nom</span><span class="sxs-lookup"><span data-stu-id="6d463-143">Name</span></span> | <span data-ttu-id="6d463-144">Description</span><span class="sxs-lookup"><span data-stu-id="6d463-144">Description</span></span> |
|-|-|
| `float3 operator+ (float3 const& value1, float3 const& value2)` | <span data-ttu-id="6d463-145">Ajoute deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="6d463-145">Adds two vectors.</span></span> |
| `float3 operator- (float3 const& value1, float3 const& value2)` | <span data-ttu-id="6d463-146">Soustrait un vecteur d’un vecteur.</span><span class="sxs-lookup"><span data-stu-id="6d463-146">Subtracts a vector from a vector.</span></span> |
| `float3 operator* (float3 const& value1, float3 const& value2)` | <span data-ttu-id="6d463-147">Multiplie les composants de deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="6d463-147">Multiplies the components of two vectors by each other.</span></span> |
| `float3 operator* (float3 const& value1, float value2)` | <span data-ttu-id="6d463-148">Multiplie un vecteur par un scalaire.</span><span class="sxs-lookup"><span data-stu-id="6d463-148">Multiplies a vector by a scalar.</span></span> |
| `float3 operator* (float value1, float3 const& value2)` | <span data-ttu-id="6d463-149">Multiplie un vecteur par un scalaire.</span><span class="sxs-lookup"><span data-stu-id="6d463-149">Multiplies a vector by a scalar.</span></span> |
| `float3 operator/ (float3 const& value1, float3 const& value2)` | <span data-ttu-id="6d463-150">Divise les composants d’un vecteur par les composants d’un autre vecteur.</span><span class="sxs-lookup"><span data-stu-id="6d463-150">Divides the components of a vector by the components of another vector.</span></span> |
| `float3 operator/ (float3 const& value1, float value2)` | <span data-ttu-id="6d463-151">Divise un vecteur par une valeur scalaire.</span><span class="sxs-lookup"><span data-stu-id="6d463-151">Divides a vector by a scalar value.</span></span> |
| `float3 operator- (float3 const& value)` | <span data-ttu-id="6d463-152">Retourne un vecteur pointant dans la direction opposée.</span><span class="sxs-lookup"><span data-stu-id="6d463-152">Returns a vector pointing in the opposite direction.</span></span> |
| `float3& operator+= (float3& value1, float3 const& value2)` | <span data-ttu-id="6d463-153">Sur place ajoute deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="6d463-153">In-place adds two vectors.</span></span> |
| `float3& operator-= (float3& value1, float3 const& value2)` | <span data-ttu-id="6d463-154">Sur place soustrait un vecteur d’un vecteur.</span><span class="sxs-lookup"><span data-stu-id="6d463-154">In-place subtracts a vector from a vector.</span></span> |
| `float3& operator*= (float3& value1, float3 const& value2)` | <span data-ttu-id="6d463-155">Sur place, multiplie les composants de deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="6d463-155">In-place multiplies the components of two vectors by each other.</span></span> |
| `float3& operator*= (float3& value1, float value2)` | <span data-ttu-id="6d463-156">Sur place, multiplie un vecteur par un scalaire.</span><span class="sxs-lookup"><span data-stu-id="6d463-156">In-place multiplies a vector by a scalar.</span></span> |
| `float3& operator/= (float3& value1, float3 const& value2)` | <span data-ttu-id="6d463-157">Sur place, divise les composants d’un vecteur par les composants d’un autre vecteur.</span><span class="sxs-lookup"><span data-stu-id="6d463-157">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float3& operator/= (float3& value1, float value2)` | <span data-ttu-id="6d463-158">Sur place divise un vecteur par une valeur scalaire.</span><span class="sxs-lookup"><span data-stu-id="6d463-158">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float3 const& value1, float3 const& value2)` | <span data-ttu-id="6d463-159">Détermine si deux instances de float3 sont égales.</span><span class="sxs-lookup"><span data-stu-id="6d463-159">Determines whether two instances of float3 are equal.</span></span> |
| `bool operator!= (float3 const& value1, float3 const& value2)` | <span data-ttu-id="6d463-160">Détermine si deux instances de float3 ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="6d463-160">Determines whether two instances of float3 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector3() const` | <span data-ttu-id="6d463-161">Convertit un float3 en un **Microsoft. Graphics. Canvas. Numerics. Vector3**.</span><span class="sxs-lookup"><span data-stu-id="6d463-161">Converts a float3 to a **Microsoft.Graphics.Canvas.Numerics.Vector3**.</span></span> |

## <a name="fields"></a><span data-ttu-id="6d463-162">Champs</span><span class="sxs-lookup"><span data-stu-id="6d463-162">Fields</span></span>

| <span data-ttu-id="6d463-163">Nom</span><span class="sxs-lookup"><span data-stu-id="6d463-163">Name</span></span> | <span data-ttu-id="6d463-164">Description</span><span class="sxs-lookup"><span data-stu-id="6d463-164">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="6d463-165">Composant X du vecteur.</span><span class="sxs-lookup"><span data-stu-id="6d463-165">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="6d463-166">Composant Y du vecteur.</span><span class="sxs-lookup"><span data-stu-id="6d463-166">Y component of the vector.</span></span> |
| `float z` | <span data-ttu-id="6d463-167">Composant Z du vecteur.</span><span class="sxs-lookup"><span data-stu-id="6d463-167">Z component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="6d463-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d463-168">Requirements</span></span>

| <span data-ttu-id="6d463-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d463-169">Requirement</span></span> | <span data-ttu-id="6d463-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d463-170">Value</span></span> |
|-|-|
| <span data-ttu-id="6d463-171">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6d463-171">Namespace</span></span> | <span data-ttu-id="6d463-172">Windows :: Foundation :: Numerics</span><span class="sxs-lookup"><span data-stu-id="6d463-172">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="6d463-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d463-173">Header</span></span> | <dl> <span data-ttu-id="6d463-174"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d463-174"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="6d463-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d463-175">See also</span></span>

[<span data-ttu-id="6d463-176">API windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="6d463-176">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
