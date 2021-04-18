---
title: float4, structure (Windowsnumerics. h)
description: Vecteur avec quatre composants.
ms.assetid: AC07C6D0-E7FD-4582-B40D-4838F49FB8B4
keywords:
- float4, structure
topic_type:
- apiref
api_name:
- float4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4a2a4721e3ab7e5520545b42367d2432ba967f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540671"
---
# <a name="float4-structure"></a><span data-ttu-id="07b47-104">float4, structure</span><span class="sxs-lookup"><span data-stu-id="07b47-104">float4 structure</span></span>

<span data-ttu-id="07b47-105">Vecteur avec quatre composants.</span><span class="sxs-lookup"><span data-stu-id="07b47-105">A vector with four components.</span></span>

<span data-ttu-id="07b47-106">Ce type est disponible uniquement en C++.</span><span class="sxs-lookup"><span data-stu-id="07b47-106">This type is available only in C++.</span></span> <span data-ttu-id="07b47-107">Son équivalent .NET est [System. Numerics. Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="07b47-107">Its .NET equivalent is [System.Numerics.Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="07b47-108">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="07b47-108">Constructors</span></span>

| <span data-ttu-id="07b47-109">Nom</span><span class="sxs-lookup"><span data-stu-id="07b47-109">Name</span></span> | <span data-ttu-id="07b47-110">Description</span><span class="sxs-lookup"><span data-stu-id="07b47-110">Description</span></span> |
|-|-|
| `float4()` | <span data-ttu-id="07b47-111">Crée un float4 non initialisé.</span><span class="sxs-lookup"><span data-stu-id="07b47-111">Creates an uninitialized float4.</span></span> |
| `float4(float x, float y, float z, float w)` | <span data-ttu-id="07b47-112">Crée un float4 avec les valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="07b47-112">Creates a float4 with the specified values.</span></span> |
| `float4(float2 value, float z, float w)` | <span data-ttu-id="07b47-113">Crée un float4 avec x et y copié à partir d’un float2 plus les valeurs z et w spécifiées.</span><span class="sxs-lookup"><span data-stu-id="07b47-113">Creates a float4 with x and y copied from a float2 plus the specified z and w values.</span></span> |
| `float4(float3 value, float w)` | <span data-ttu-id="07b47-114">Crée un float4 avec x, y et z copié à partir d’un float3 plus la valeur w spécifiée.</span><span class="sxs-lookup"><span data-stu-id="07b47-114">Creates a float4 with x, y and z copied from a float3 plus the specified w value.</span></span> |
| `explicit float4(float value)` | <span data-ttu-id="07b47-115">Crée un float4 avec l’ensemble de com. travau défini sur la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="07b47-115">Creates a float4 with all com.ents set to the specified value.</span></span> |
| `float4(Microsoft::?Graphics::?Canvas::?Numerics::?Vector4 const& value)` | <span data-ttu-id="07b47-116">Convertit un **Microsoft. Graphics. canevas. Numerics. Vector4** en float4.</span><span class="sxs-lookup"><span data-stu-id="07b47-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector4** to a float4.</span></span> |

## <a name="functions"></a><span data-ttu-id="07b47-117">Fonctions</span><span class="sxs-lookup"><span data-stu-id="07b47-117">Functions</span></span>

| <span data-ttu-id="07b47-118">Nom</span><span class="sxs-lookup"><span data-stu-id="07b47-118">Name</span></span> | <span data-ttu-id="07b47-119">Description</span><span class="sxs-lookup"><span data-stu-id="07b47-119">Description</span></span> |
|-|-|
| `float length(float4 const& value)` | <span data-ttu-id="07b47-120">Calcule la longueur, ou distance euclidienne, du vecteur.</span><span class="sxs-lookup"><span data-stu-id="07b47-120">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float4 const& value)` | <span data-ttu-id="07b47-121">Calcule la longueur, ou distance euclidienne, du vecteur carré.</span><span class="sxs-lookup"><span data-stu-id="07b47-121">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float4 const& value1, float4 const& value2)` | <span data-ttu-id="07b47-122">Calcule la distance euclidienne entre deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="07b47-122">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float4 const& value1, float4 const& value2)` | <span data-ttu-id="07b47-123">Calcule la distance euclidienne entre deux vecteurs carrés.</span><span class="sxs-lookup"><span data-stu-id="07b47-123">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float4 const& vector1, float4 const& vector2)` | <span data-ttu-id="07b47-124">Calcule le produit scalaire de deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="07b47-124">Calculates the dot product of two vectors.</span></span> |
| `float4 normalize(float4 const& vector)` | <span data-ttu-id="07b47-125">Crée un vecteur d’unité à partir du vecteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="07b47-125">Creates a unit vector from the specified vector.</span></span> |
| `float4 min(float4 const& value1, float4 const& value2)` | <span data-ttu-id="07b47-126">Retourne un vecteur qui contient la valeur la plus faible de chaque paire de composants correspondante.</span><span class="sxs-lookup"><span data-stu-id="07b47-126">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float4 max(float4 const& value1, float4 const& value2)` | <span data-ttu-id="07b47-127">Retourne un vecteur qui contient la valeur la plus élevée de chaque paire de composants correspondante.</span><span class="sxs-lookup"><span data-stu-id="07b47-127">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float4 clamp(float4 const& value1, float4 const& min, float4 const& max)` | <span data-ttu-id="07b47-128">Restreint une valeur à une plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="07b47-128">Restricts a value to be within a specified range.</span></span> |
| `float4 lerp(float4 const& value1, float4 const& value2, float amount)` | <span data-ttu-id="07b47-129">Effectue une interpolation linéaire entre deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="07b47-129">Performs a linear interpolation between two vectors.</span></span> |
| `float4 transform(float4 const& vector, float4x4 const& matrix)` | <span data-ttu-id="07b47-130">Transforme un float4 par la matrice donnée.</span><span class="sxs-lookup"><span data-stu-id="07b47-130">Transforms a float4 by the given matrix.</span></span> |
| `float4 transform4(float3 const& position, float4x4 const& matrix)` | <span data-ttu-id="07b47-131">Transforme un float3 par la matrice donnée, en retournant un float4.</span><span class="sxs-lookup"><span data-stu-id="07b47-131">Transforms a float3 by the given matrix, returning a float4.</span></span> |
| `float4 transform4(float2 const& position, float4x4 const& matrix)` | <span data-ttu-id="07b47-132">Transforme un float2 par la matrice donnée, en retournant un float4.</span><span class="sxs-lookup"><span data-stu-id="07b47-132">Transforms a float2 by the given matrix, returning a float4.</span></span> |
| `float4 transform(float4 const& value, quaternion const& rotation)` | <span data-ttu-id="07b47-133">Transforme un float4 par le Quaternion donné.</span><span class="sxs-lookup"><span data-stu-id="07b47-133">Transforms a float4 by the given quaternion.</span></span> |
| `float4 transform4(float3 const& value, quaternion const& rotation)` | <span data-ttu-id="07b47-134">Transforme un float3 par le Quaternion donné, en retournant un float4.</span><span class="sxs-lookup"><span data-stu-id="07b47-134">Transforms a float3 by the given quaternion, returning a float4.</span></span> |
| `float4 transform4(float2 const& value, quaternion const& rotation)` | <span data-ttu-id="07b47-135">Transforme un float2 par le Quaternion donné, en retournant un float4.</span><span class="sxs-lookup"><span data-stu-id="07b47-135">Transforms a float2 by the given quaternion, returning a float4.</span></span> |

## <a name="methods"></a><span data-ttu-id="07b47-136">Méthodes</span><span class="sxs-lookup"><span data-stu-id="07b47-136">Methods</span></span>

| <span data-ttu-id="07b47-137">Nom</span><span class="sxs-lookup"><span data-stu-id="07b47-137">Name</span></span> | <span data-ttu-id="07b47-138">Description</span><span class="sxs-lookup"><span data-stu-id="07b47-138">Description</span></span> |
|-|-|
| `static float4 zero()` | <span data-ttu-id="07b47-139">Retourne un float4 avec tous ses composants définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="07b47-139">Returns a float4 with all of its components set to zero.</span></span> |
| `static float4 one()` | <span data-ttu-id="07b47-140">Retourne un float4 avec tous ses composants définis sur un.</span><span class="sxs-lookup"><span data-stu-id="07b47-140">Returns a float4 with all of its components set to one.</span></span> |
| `static float4 unit_x()` | <span data-ttu-id="07b47-141">Retourne float4 (1, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="07b47-141">Returns the float4 (1, 0, 0, 0).</span></span> |
| `static float4 unit_y()` | <span data-ttu-id="07b47-142">Retourne float4 (0, 1, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="07b47-142">Returns the float4 (0, 1, 0, 0).</span></span> |
| `static float4 unit_z()` | <span data-ttu-id="07b47-143">Retourne le float4 (0, 0, 1, 0).</span><span class="sxs-lookup"><span data-stu-id="07b47-143">Returns the float4 (0, 0, 1, 0).</span></span> |
| `static float4 unit_w()` | <span data-ttu-id="07b47-144">Retourne le float4 (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="07b47-144">Returns the float4 (0, 0, 0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="07b47-145">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="07b47-145">Operators</span></span>

| <span data-ttu-id="07b47-146">Nom</span><span class="sxs-lookup"><span data-stu-id="07b47-146">Name</span></span> | <span data-ttu-id="07b47-147">Description</span><span class="sxs-lookup"><span data-stu-id="07b47-147">Description</span></span> |
|-|-|
| `float4 operator+ (float4 const& value1, float4 const& value2)` | <span data-ttu-id="07b47-148">Ajoute deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="07b47-148">Adds two vectors.</span></span> |
| `float4 operator- (float4 const& value1, float4 const& value2)` | <span data-ttu-id="07b47-149">Soustrait un vecteur d’un vecteur.</span><span class="sxs-lookup"><span data-stu-id="07b47-149">Subtracts a vector from a vector.</span></span> |
| `float4 operator* (float4 const& value1, float4 const& value2)` | <span data-ttu-id="07b47-150">Multiplie les composants de deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="07b47-150">Multiplies the components of two vectors by each other.</span></span> |
| `float4 operator* (float4 const& value1, float value2)` | <span data-ttu-id="07b47-151">Multiplie un vecteur par un scalaire.</span><span class="sxs-lookup"><span data-stu-id="07b47-151">Multiplies a vector by a scalar.</span></span> |
| `float4 operator* (float value1, float4 const& value2)` | <span data-ttu-id="07b47-152">Multiplie un vecteur par un scalaire.</span><span class="sxs-lookup"><span data-stu-id="07b47-152">Multiplies a vector by a scalar.</span></span> |
| `float4 operator/ (float4 const& value1, float4 const& value2)` | <span data-ttu-id="07b47-153">Divise les composants d’un vecteur par les composants d’un autre vecteur.</span><span class="sxs-lookup"><span data-stu-id="07b47-153">Divides the components of a vector by the components of another vector.</span></span> |
| `float4 operator/ (float4 const& value1, float value2)` | <span data-ttu-id="07b47-154">Divise un vecteur par une valeur scalaire.</span><span class="sxs-lookup"><span data-stu-id="07b47-154">Divides a vector by a scalar value.</span></span> |
| `float4 operator- (float4 const& value)` | <span data-ttu-id="07b47-155">Retourne un vecteur pointant dans la direction opposée.</span><span class="sxs-lookup"><span data-stu-id="07b47-155">Returns a vector pointing in the opposite direction.</span></span> |
| `float4& operator+= (float4& value1, float4 const& value2)` | <span data-ttu-id="07b47-156">Sur place ajoute deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="07b47-156">In-place adds two vectors.</span></span> |
| `float4& operator-= (float4& value1, float4 const& value2)` | <span data-ttu-id="07b47-157">Sur place soustrait un vecteur d’un vecteur.</span><span class="sxs-lookup"><span data-stu-id="07b47-157">In-place subtracts a vector from a vector.</span></span> |
| `float4& operator*= (float4& value1, float4 const& value2)` | <span data-ttu-id="07b47-158">Sur place, multiplie les composants de deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="07b47-158">In-place multiplies the components of two vectors by each other.</span></span> |
| `float4& operator*= (float4& value1, float value2)` | <span data-ttu-id="07b47-159">Sur place, multiplie un vecteur par un scalaire.</span><span class="sxs-lookup"><span data-stu-id="07b47-159">In-place multiplies a vector by a scalar.</span></span> |
| `float4& operator/= (float4& value1, float4 const& value2)` | <span data-ttu-id="07b47-160">Sur place, divise les composants d’un vecteur par les composants d’un autre vecteur.</span><span class="sxs-lookup"><span data-stu-id="07b47-160">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float4& operator/= (float4& value1, float value2)` | <span data-ttu-id="07b47-161">Sur place divise un vecteur par une valeur scalaire.</span><span class="sxs-lookup"><span data-stu-id="07b47-161">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float4 const& value1, float4 const& value2)` | <span data-ttu-id="07b47-162">Détermine si deux instances de float4 sont égales.</span><span class="sxs-lookup"><span data-stu-id="07b47-162">Determines whether two instances of float4 are equal.</span></span> |
| `bool operator!= (float4 const& value1, float4 const& value2)` | <span data-ttu-id="07b47-163">Détermine si deux instances de float4 ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="07b47-163">Determines whether two instances of float4 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector4() const` | <span data-ttu-id="07b47-164">Convertit un float4 en un **Microsoft. Graphics. Canvas. Numerics. Vector4**.</span><span class="sxs-lookup"><span data-stu-id="07b47-164">Converts a float4 to a **Microsoft.Graphics.Canvas.Numerics.Vector4**.</span></span> |

## <a name="fields"></a><span data-ttu-id="07b47-165">Champs</span><span class="sxs-lookup"><span data-stu-id="07b47-165">Fields</span></span>

| <span data-ttu-id="07b47-166">Nom</span><span class="sxs-lookup"><span data-stu-id="07b47-166">Name</span></span> | <span data-ttu-id="07b47-167">Description</span><span class="sxs-lookup"><span data-stu-id="07b47-167">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="07b47-168">Composant X du vecteur.</span><span class="sxs-lookup"><span data-stu-id="07b47-168">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="07b47-169">Composant Y du vecteur.</span><span class="sxs-lookup"><span data-stu-id="07b47-169">Y component of the vector.</span></span> |
| `float z` | <span data-ttu-id="07b47-170">Composant Z du vecteur.</span><span class="sxs-lookup"><span data-stu-id="07b47-170">Z component of the vector.</span></span> |
| `float w` | <span data-ttu-id="07b47-171">Composant W du vecteur.</span><span class="sxs-lookup"><span data-stu-id="07b47-171">W component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="07b47-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07b47-172">Requirements</span></span>

| <span data-ttu-id="07b47-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07b47-173">Requirement</span></span> | <span data-ttu-id="07b47-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="07b47-174">Value</span></span> |
|-|-|
| <span data-ttu-id="07b47-175">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="07b47-175">Namespace</span></span> | <span data-ttu-id="07b47-176">Windows :: Foundation :: Numerics</span><span class="sxs-lookup"><span data-stu-id="07b47-176">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="07b47-177">En-tête</span><span class="sxs-lookup"><span data-stu-id="07b47-177">Header</span></span> | <dl> <span data-ttu-id="07b47-178"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="07b47-178"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="07b47-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07b47-179">See also</span></span>

[<span data-ttu-id="07b47-180">API windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="07b47-180">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
