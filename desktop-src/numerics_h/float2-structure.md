---
title: float2, structure (Windowsnumerics. h)
description: Vecteur avec deux composants.
ms.assetid: 1A23C1E3-F34F-4249-80EA-92A13CD4B34F
keywords:
- float2, structure
topic_type:
- apiref
api_name:
- float2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72398bdc087e0f7a0845703a2cefea40b5465b21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525638"
---
# <a name="float2-structure"></a><span data-ttu-id="764f9-104">float2, structure</span><span class="sxs-lookup"><span data-stu-id="764f9-104">float2 structure</span></span>

<span data-ttu-id="764f9-105">Vecteur avec deux composants.</span><span class="sxs-lookup"><span data-stu-id="764f9-105">A vector with two components.</span></span>

<span data-ttu-id="764f9-106">Ce type est disponible uniquement en C++.</span><span class="sxs-lookup"><span data-stu-id="764f9-106">This type is available only in C++.</span></span> <span data-ttu-id="764f9-107">Son équivalent .NET est [System. Numerics. Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="764f9-107">Its .NET equivalent is [System.Numerics.Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="764f9-108">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="764f9-108">Constructors</span></span>

| <span data-ttu-id="764f9-109">Nom</span><span class="sxs-lookup"><span data-stu-id="764f9-109">Name</span></span> | <span data-ttu-id="764f9-110">Description</span><span class="sxs-lookup"><span data-stu-id="764f9-110">Description</span></span> |
|-|-|
| `float2()` | <span data-ttu-id="764f9-111">Crée un float2 non initialisé.</span><span class="sxs-lookup"><span data-stu-id="764f9-111">Creates an uninitialized float2.</span></span> |
| `float2(float x, float y)` | <span data-ttu-id="764f9-112">Crée un float2 avec les valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="764f9-112">Creates a float2 with the specified values.</span></span> |
| `explicit float2(float value)` | <span data-ttu-id="764f9-113">Crée un float2 avec tous les composants définis sur la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="764f9-113">Creates a float2 with all components set to the specified value.</span></span> |
| `float2(Microsoft::Graphics::Canvas::Numerics::Vector2 const& value)` | <span data-ttu-id="764f9-114">Convertit un **Microsoft. Graphics. canevas. Numerics. Vector2** en float2.</span><span class="sxs-lookup"><span data-stu-id="764f9-114">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector2** to a float2.</span></span> |
| `float2(Windows::Foundation::Point const& value)` | <span data-ttu-id="764f9-115">Convertit un [**Windows. Foundation. point**](/uwp/api/Windows.Foundation.Point) en float2.</span><span class="sxs-lookup"><span data-stu-id="764f9-115">Converts a [**Windows.Foundation.Point**](/uwp/api/Windows.Foundation.Point) to a float2.</span></span> |
| `float2(Windows::Foundation::Size const& value)` | <span data-ttu-id="764f9-116">Convertit [**Windows. Foundation. Size**](/uwp/api/Windows.Foundation.Size) en float2.</span><span class="sxs-lookup"><span data-stu-id="764f9-116">Converts a [**Windows.Foundation.Size**](/uwp/api/Windows.Foundation.Size) to a float2.</span></span> |

## <a name="functions"></a><span data-ttu-id="764f9-117">Fonctions</span><span class="sxs-lookup"><span data-stu-id="764f9-117">Functions</span></span>

| <span data-ttu-id="764f9-118">Nom</span><span class="sxs-lookup"><span data-stu-id="764f9-118">Name</span></span> | <span data-ttu-id="764f9-119">Description</span><span class="sxs-lookup"><span data-stu-id="764f9-119">Description</span></span> |
|-|-|
| `float length(float2 const& value)` | <span data-ttu-id="764f9-120">Calcule la longueur, ou distance euclidienne, du vecteur.</span><span class="sxs-lookup"><span data-stu-id="764f9-120">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float2 const& value)` | <span data-ttu-id="764f9-121">Calcule la longueur, ou distance euclidienne, du vecteur carré.</span><span class="sxs-lookup"><span data-stu-id="764f9-121">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float2 const& value1, float2 const& value2)` | <span data-ttu-id="764f9-122">Calcule la distance euclidienne entre deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="764f9-122">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float2 const& value1, float2 const& value2)` | <span data-ttu-id="764f9-123">Calcule la distance euclidienne entre deux vecteurs carrés.</span><span class="sxs-lookup"><span data-stu-id="764f9-123">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float2 const& value1, float2 const& value2)` | <span data-ttu-id="764f9-124">Calcule le produit scalaire de deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="764f9-124">Calculates the dot product of two vectors.</span></span> |
| `float2 normalize(float2 const& value)` | <span data-ttu-id="764f9-125">Crée un vecteur d’unité à partir du vecteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="764f9-125">Creates a unit vector from the specified vector.</span></span> |
| `float2 reflect(float2 const& vector, float2 const& normal)` | <span data-ttu-id="764f9-126">Détermine le vecteur réfléchissant du vecteur donné et normal.</span><span class="sxs-lookup"><span data-stu-id="764f9-126">Determines the reflect vector of the given vector and normal.</span></span> |
| `float2 min(float2 const& value1, float2 const& value2)` | <span data-ttu-id="764f9-127">Retourne un vecteur qui contient la valeur la plus faible de chaque paire de composants correspondante.</span><span class="sxs-lookup"><span data-stu-id="764f9-127">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float2 max(float2 const& value1, float2 const& value2)` | <span data-ttu-id="764f9-128">Retourne un vecteur qui contient la valeur la plus élevée de chaque paire de composants correspondante.</span><span class="sxs-lookup"><span data-stu-id="764f9-128">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float2 clamp(float2 const& value1, float2 const& min, float2 const& max)` | <span data-ttu-id="764f9-129">Restreint une valeur à une plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="764f9-129">Restricts a value to be within a specified range.</span></span> |
| `float2 lerp(float2 const& value1, float2 const& value2, float amount)` | <span data-ttu-id="764f9-130">Effectue une interpolation linéaire entre deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="764f9-130">Performs a linear interpolation between two vectors.</span></span> |
| `float2 transform(float2 const& position, float3x2 const& matrix)` | <span data-ttu-id="764f9-131">Transforme le vecteur (x, y, 0, 1) par la matrice spécifiée.</span><span class="sxs-lookup"><span data-stu-id="764f9-131">Transforms the vector (x, y, 0, 1) by the specified matrix.</span></span> |
| `float2 transform(float2 const& position, float4x4 const& matrix)` | <span data-ttu-id="764f9-132">Transforme le vecteur (x, y, 0, 1) par la matrice spécifiée.</span><span class="sxs-lookup"><span data-stu-id="764f9-132">Transforms the vector (x, y, 0, 1) by the specified matrix.</span></span> |
| `float2 transform_normal(float2 const& normal, float3x2 const& matrix)` | <span data-ttu-id="764f9-133">Transforme le vecteur normal (x, y, 0, 0) par la matrice spécifiée.</span><span class="sxs-lookup"><span data-stu-id="764f9-133">Transforms the normal vector (x, y, 0, 0) by the specified matrix.</span></span> |
| `float2 transform_normal(float2 const& normal, float4x4 const& matrix)` | <span data-ttu-id="764f9-134">Transforme le vecteur normal (x, y, 0, 0) par la matrice spécifiée.</span><span class="sxs-lookup"><span data-stu-id="764f9-134">Transforms the normal vector (x, y, 0, 0) by the specified matrix.</span></span> |
| `float2 transform(float2 const& value, quaternion const& rotation)` | <span data-ttu-id="764f9-135">Transforme un float2 par le Quaternion donné.</span><span class="sxs-lookup"><span data-stu-id="764f9-135">Transforms a float2 by the given quaternion.</span></span> |

## <a name="methods"></a><span data-ttu-id="764f9-136">Méthodes</span><span class="sxs-lookup"><span data-stu-id="764f9-136">Methods</span></span>

| <span data-ttu-id="764f9-137">Nom</span><span class="sxs-lookup"><span data-stu-id="764f9-137">Name</span></span> | <span data-ttu-id="764f9-138">Description</span><span class="sxs-lookup"><span data-stu-id="764f9-138">Description</span></span> |
|-|-|
| `static float2 zero()` | <span data-ttu-id="764f9-139">Retourne un float2 avec tous ses composants définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="764f9-139">Returns a float2 with all of its components set to zero.</span></span> |
| `static float2 one()` | <span data-ttu-id="764f9-140">Retourne un float2 avec tous ses composants définis sur un.</span><span class="sxs-lookup"><span data-stu-id="764f9-140">Returns a float2 with all of its components set to one.</span></span> |
| `static float2 unit_x()` | <span data-ttu-id="764f9-141">Retourne le float2 (1,0).</span><span class="sxs-lookup"><span data-stu-id="764f9-141">Returns the float2 (1, 0).</span></span> |
| `static float2 unit_y()` | <span data-ttu-id="764f9-142">Retourne le float2 (0, 1).</span><span class="sxs-lookup"><span data-stu-id="764f9-142">Returns the float2 (0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="764f9-143">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="764f9-143">Operators</span></span>

| <span data-ttu-id="764f9-144">Nom</span><span class="sxs-lookup"><span data-stu-id="764f9-144">Name</span></span> | <span data-ttu-id="764f9-145">Description</span><span class="sxs-lookup"><span data-stu-id="764f9-145">Description</span></span> |
|-|-|
| `operator Windows::Foundation::Point() const` | <span data-ttu-id="764f9-146">Convertit un float2 en un [**Windows. Foundation. point**](/uwp/api/Windows.Foundation.Point).</span><span class="sxs-lookup"><span data-stu-id="764f9-146">Converts a float2 to a [**Windows.Foundation.Point**](/uwp/api/Windows.Foundation.Point).</span></span> |
| `operator Windows::Foundation::Size() const` | <span data-ttu-id="764f9-147">Convertit un float2 en un [**Windows. Foundation. Size**](/uwp/api/Windows.Foundation.Size).</span><span class="sxs-lookup"><span data-stu-id="764f9-147">Converts a float2 to a [**Windows.Foundation.Size**](/uwp/api/Windows.Foundation.Size).</span></span> |
| `float2 operator+ (float2 const& value1, float2 const& value2)` | <span data-ttu-id="764f9-148">Ajoute deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="764f9-148">Adds two vectors.</span></span> |
| `float2 operator- (float2 const& value1, float2 const& value2)` | <span data-ttu-id="764f9-149">Soustrait un vecteur d’un vecteur.</span><span class="sxs-lookup"><span data-stu-id="764f9-149">Subtracts a vector from a vector.</span></span> |
| `float2 operator* (float2 const& value1, float2 const& value2)` | <span data-ttu-id="764f9-150">Multiplie les composants de deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="764f9-150">Multiplies the components of two vectors by each other.</span></span> |
| `float2 operator* (float2 const& value1, float value2)` | <span data-ttu-id="764f9-151">Multiplie un vecteur par un scalaire.</span><span class="sxs-lookup"><span data-stu-id="764f9-151">Multiplies a vector by a scalar.</span></span> |
| `float2 operator* (float value1, float2 const& value2)` | <span data-ttu-id="764f9-152">Multiplie un vecteur par un scalaire.</span><span class="sxs-lookup"><span data-stu-id="764f9-152">Multiplies a vector by a scalar.</span></span> |
| `float2 operator/ (float2 const& value1, float2 const& value2)` | <span data-ttu-id="764f9-153">Divise les composants d’un vecteur par les composants d’un autre vecteur.</span><span class="sxs-lookup"><span data-stu-id="764f9-153">Divides the components of a vector by the components of another vector.</span></span> |
| `float2 operator/ (float2 const& value1, float value2)` | <span data-ttu-id="764f9-154">Divise un vecteur par une valeur scalaire.</span><span class="sxs-lookup"><span data-stu-id="764f9-154">Divides a vector by a scalar value.</span></span> |
| `float2 operator- (float2 const& value)` | <span data-ttu-id="764f9-155">Retourne un vecteur pointant dans la direction opposée.</span><span class="sxs-lookup"><span data-stu-id="764f9-155">Returns a vector pointing in the opposite direction.</span></span> |
| `float2& operator+= (float2& value1, float2 const& value2)` | <span data-ttu-id="764f9-156">Sur place ajoute deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="764f9-156">In-place adds two vectors.</span></span> |
| `float2& operator-= (float2& value1, float2 const& value2)` | <span data-ttu-id="764f9-157">Sur place soustrait un vecteur d’un vecteur.</span><span class="sxs-lookup"><span data-stu-id="764f9-157">In-place subtracts a vector from a vector.</span></span> |
| `float2& operator*= (float2& value1, float2 const& value2)` | <span data-ttu-id="764f9-158">Sur place, multiplie les composants de deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="764f9-158">In-place multiplies the components of two vectors by each other.</span></span> |
| `float2& operator*= (float2& value1, float value2)` | <span data-ttu-id="764f9-159">Sur place, multiplie un vecteur par un scalaire.</span><span class="sxs-lookup"><span data-stu-id="764f9-159">In-place multiplies a vector by a scalar.</span></span> |
| `float2& operator/= (float2& value1, float2 const& value2)` | <span data-ttu-id="764f9-160">Sur place, divise les composants d’un vecteur par les composants d’un autre vecteur.</span><span class="sxs-lookup"><span data-stu-id="764f9-160">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float2& operator/= (float2& value1, float value2)` | <span data-ttu-id="764f9-161">Sur place divise un vecteur par une valeur scalaire.</span><span class="sxs-lookup"><span data-stu-id="764f9-161">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float2 const& value1, float2 const& value2)` | <span data-ttu-id="764f9-162">Détermine si deux instances de float2 sont égales.</span><span class="sxs-lookup"><span data-stu-id="764f9-162">Determines whether two instances of float2 are equal.</span></span> |
| `bool operator!= (float2 const& value1, float2 const& value2)` | <span data-ttu-id="764f9-163">Détermine si deux instances de float2 ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="764f9-163">Determines whether two instances of float2 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector2() const` | <span data-ttu-id="764f9-164">Convertit un float2 en un **Microsoft. Graphics. Canvas. Numerics. Vector2**.</span><span class="sxs-lookup"><span data-stu-id="764f9-164">Converts a float2 to a **Microsoft.Graphics.Canvas.Numerics.Vector2**.</span></span> |

## <a name="fields"></a><span data-ttu-id="764f9-165">Champs</span><span class="sxs-lookup"><span data-stu-id="764f9-165">Fields</span></span>

| <span data-ttu-id="764f9-166">Nom</span><span class="sxs-lookup"><span data-stu-id="764f9-166">Name</span></span> | <span data-ttu-id="764f9-167">Description</span><span class="sxs-lookup"><span data-stu-id="764f9-167">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="764f9-168">Composant X du vecteur.</span><span class="sxs-lookup"><span data-stu-id="764f9-168">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="764f9-169">Composant Y du vecteur.</span><span class="sxs-lookup"><span data-stu-id="764f9-169">Y component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="764f9-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="764f9-170">Requirements</span></span>

| <span data-ttu-id="764f9-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="764f9-171">Requirement</span></span> | <span data-ttu-id="764f9-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="764f9-172">Value</span></span> |
|-|-|
| <span data-ttu-id="764f9-173">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="764f9-173">Namespace</span></span> | <span data-ttu-id="764f9-174">Windows :: Foundation :: Numerics</span><span class="sxs-lookup"><span data-stu-id="764f9-174">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="764f9-175">En-tête</span><span class="sxs-lookup"><span data-stu-id="764f9-175">Header</span></span> | <dl> <span data-ttu-id="764f9-176"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="764f9-176"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="764f9-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="764f9-177">See also</span></span>

[<span data-ttu-id="764f9-178">API windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="764f9-178">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
