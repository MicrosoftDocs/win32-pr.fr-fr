---
title: float3x2, structure (Windowsnumerics. h)
description: Matrice matrice, utilisée pour les transformations 2D.
ms.assetid: 5C2A4C30-3EC4-4DE9-A42A-6A19F96F8D69
keywords:
- float3x2, structure
topic_type:
- apiref
api_name:
- float3x2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9351fae9636ca2512825c7df5383eddf1558583e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544050"
---
# <a name="float3x2-structure"></a><span data-ttu-id="92033-104">float3x2, structure</span><span class="sxs-lookup"><span data-stu-id="92033-104">float3x2 structure</span></span>

<span data-ttu-id="92033-105">Matrice matrice, utilisée pour les transformations 2D.</span><span class="sxs-lookup"><span data-stu-id="92033-105">A 3x2 matrix, used for 2D transforms.</span></span>

<span data-ttu-id="92033-106">Ce type de matrice utilise une disposition de vecteur de ligne.</span><span class="sxs-lookup"><span data-stu-id="92033-106">This matrix type uses a row vector layout.</span></span> <span data-ttu-id="92033-107">Les coordonnées x et y du vecteur de translation de cette matrice correspondent aux champs M31, M32.</span><span class="sxs-lookup"><span data-stu-id="92033-107">The x and y of this matrix's translation vector correspond to the fields m31, m32.</span></span>

<span data-ttu-id="92033-108">Ce type est disponible uniquement en C++.</span><span class="sxs-lookup"><span data-stu-id="92033-108">This type is available only in C++.</span></span> <span data-ttu-id="92033-109">Son équivalent .NET est [System. Numerics. Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="92033-109">Its .NET equivalent is [System.Numerics.Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="92033-110">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="92033-110">Constructors</span></span>

| <span data-ttu-id="92033-111">Nom</span><span class="sxs-lookup"><span data-stu-id="92033-111">Name</span></span> | <span data-ttu-id="92033-112">Description</span><span class="sxs-lookup"><span data-stu-id="92033-112">Description</span></span> |
|-|-|
| `float3x2()` | <span data-ttu-id="92033-113">Crée un float3x2 non initialisé.</span><span class="sxs-lookup"><span data-stu-id="92033-113">Creates an uninitialized float3x2.</span></span> |
| `float3x2(float m11, float m12, float m21, float m22, float m31, float m32)` | <span data-ttu-id="92033-114">Crée un float3x2 avec les valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="92033-114">Creates a float3x2 with the specified values.</span></span> |
| `float3x2(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2 const& value)` | <span data-ttu-id="92033-115">Convertit un **Microsoft. Graphics. canevas. Numerics. Matrix3x2** en float3x2.</span><span class="sxs-lookup"><span data-stu-id="92033-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Matrix3x2** to a float3x2.</span></span> |

## <a name="functions"></a><span data-ttu-id="92033-116">Fonctions</span><span class="sxs-lookup"><span data-stu-id="92033-116">Functions</span></span>

| <span data-ttu-id="92033-117">Nom</span><span class="sxs-lookup"><span data-stu-id="92033-117">Name</span></span> | <span data-ttu-id="92033-118">Description</span><span class="sxs-lookup"><span data-stu-id="92033-118">Description</span></span> |
|-|-|
| `float3x2 make_float3x2_translation(float2 const& position)` | <span data-ttu-id="92033-119">Crée une matrice de translation.</span><span class="sxs-lookup"><span data-stu-id="92033-119">Creates a translation matrix.</span></span> |
| `float3x2 make_float3x2_translation(float xPosition, float yPosition)` | <span data-ttu-id="92033-120">Crée une matrice de translation.</span><span class="sxs-lookup"><span data-stu-id="92033-120">Creates a translation matrix.</span></span> |
| `float3x2 make_float3x2_scale(float xScale, float yScale)` | <span data-ttu-id="92033-121">Crée une matrice de mise à l’échelle, centrée sur l’origine.</span><span class="sxs-lookup"><span data-stu-id="92033-121">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float xScale, float yScale, float2 const& centerPoint)` | <span data-ttu-id="92033-122">Crée une matrice de mise à l’échelle, centrée sur le point spécifié.</span><span class="sxs-lookup"><span data-stu-id="92033-122">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_scale(float2 const& scales)` | <span data-ttu-id="92033-123">Crée une matrice de mise à l’échelle, centrée sur l’origine.</span><span class="sxs-lookup"><span data-stu-id="92033-123">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float2 const& scales, float2 const& centerPoint)` | <span data-ttu-id="92033-124">Crée une matrice de mise à l’échelle, centrée sur le point spécifié.</span><span class="sxs-lookup"><span data-stu-id="92033-124">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_scale(float scale)` | <span data-ttu-id="92033-125">Crée une matrice de mise à l’échelle, centrée sur l’origine.</span><span class="sxs-lookup"><span data-stu-id="92033-125">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float scale, float2 const& centerPoint)` | <span data-ttu-id="92033-126">Crée une matrice de mise à l’échelle, centrée sur le point spécifié.</span><span class="sxs-lookup"><span data-stu-id="92033-126">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY)` | <span data-ttu-id="92033-127">Crée une matrice inclinée, centrée sur l’origine.</span><span class="sxs-lookup"><span data-stu-id="92033-127">Creates a skew matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY, float2 const& centerPoint)` | <span data-ttu-id="92033-128">Crée une matrice d’inclinaison, centrée sur le point spécifié.</span><span class="sxs-lookup"><span data-stu-id="92033-128">Creates a skew matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_rotation(float radians)` | <span data-ttu-id="92033-129">Crée une matrice de rotation, centrée sur l’origine.</span><span class="sxs-lookup"><span data-stu-id="92033-129">Creates a rotation matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_rotation(float radians, float2 const& centerPoint)` | <span data-ttu-id="92033-130">Crée une matrice de rotation, centrée sur le point spécifié.</span><span class="sxs-lookup"><span data-stu-id="92033-130">Creates a rotation matrix, centered on the specified point.</span></span> |
| `bool is_identity(float3x2 const& value)` | <span data-ttu-id="92033-131">Vérifie s’il s’agit d’une matrice d’identité.</span><span class="sxs-lookup"><span data-stu-id="92033-131">Checks whether this is an identity matrix.</span></span> |
| `float determinant(float3x2 const& value)` | <span data-ttu-id="92033-132">Calcule le déterminant de la matrice.</span><span class="sxs-lookup"><span data-stu-id="92033-132">Calculates the determinant of the matrix.</span></span> |
| `float2 translation(float3x2 const& value)` | <span data-ttu-id="92033-133">Obtient le vecteur de translation de la matrice.</span><span class="sxs-lookup"><span data-stu-id="92033-133">Gets the translation vector of the matrix.</span></span> |
| `bool invert(float3x2 const& matrix, _Out_ float3x2* result)` | <span data-ttu-id="92033-134">Calcule l’inverse d’une matrice.</span><span class="sxs-lookup"><span data-stu-id="92033-134">Calculates the inverse of a matrix.</span></span> <span data-ttu-id="92033-135">Retourne la valeur true si la matrice peut être inversée ; false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="92033-135">Returns true if the matrix can be inverted; false otherwise.</span></span> |
| `float3x2 lerp(float3x2 const& matrix1, float3x2 const& matrix2, float amount)` | <span data-ttu-id="92033-136">Interpole de manière linéaire entre les valeurs correspondantes de deux matrices.</span><span class="sxs-lookup"><span data-stu-id="92033-136">Linearly interpolates between the corresponding values of two matrices.</span></span> |

## <a name="methods"></a><span data-ttu-id="92033-137">Méthodes</span><span class="sxs-lookup"><span data-stu-id="92033-137">Methods</span></span>

| <span data-ttu-id="92033-138">Nom</span><span class="sxs-lookup"><span data-stu-id="92033-138">Name</span></span> | <span data-ttu-id="92033-139">Description</span><span class="sxs-lookup"><span data-stu-id="92033-139">Description</span></span> |
|-|-|
| `static float3x2 identity()` | <span data-ttu-id="92033-140">Retourne une instance de la matrice d’identité.</span><span class="sxs-lookup"><span data-stu-id="92033-140">Returns an instance of the identity matrix.</span></span> |

## <a name="operators"></a><span data-ttu-id="92033-141">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="92033-141">Operators</span></span>

| <span data-ttu-id="92033-142">Nom</span><span class="sxs-lookup"><span data-stu-id="92033-142">Name</span></span> | <span data-ttu-id="92033-143">Description</span><span class="sxs-lookup"><span data-stu-id="92033-143">Description</span></span> |
|-|-|
| `float3x2 operator+ (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="92033-144">Ajoute chaque composant d’une matrice à une autre matrice.</span><span class="sxs-lookup"><span data-stu-id="92033-144">Adds each component of a matrix to another matrix.</span></span> |
| `float3x2 operator- (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="92033-145">Soustrait chaque composant d’une matrice d’une autre matrice.</span><span class="sxs-lookup"><span data-stu-id="92033-145">Subtracts each component of a matrix from another matrix.</span></span> |
| `float3x2 operator* (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="92033-146">Multiplie une matrice par une autre matrice.</span><span class="sxs-lookup"><span data-stu-id="92033-146">Multiplies a matrix by another matrix.</span></span> <span data-ttu-id="92033-147">Cela a pour effet de concaténer deux transformations.</span><span class="sxs-lookup"><span data-stu-id="92033-147">This has the effect of concatenating two transforms.</span></span> |
| `float3x2 operator* (float3x2 const& value1, float value2)` | <span data-ttu-id="92033-148">Multiplie chaque composant d’une matrice par une valeur scalaire.</span><span class="sxs-lookup"><span data-stu-id="92033-148">Multiplies each component of a matrix by a scalar value.</span></span> |
| `float3x2 operator- (float3x2 const& value)` | <span data-ttu-id="92033-149">Nie chaque composant d’une matrice.</span><span class="sxs-lookup"><span data-stu-id="92033-149">Negates each component of a matrix.</span></span> |
| `float3x2& operator+= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="92033-150">Sur place ajoute chaque composant d’une matrice à une autre matrice.</span><span class="sxs-lookup"><span data-stu-id="92033-150">In-place adds each component of a matrix to another matrix.</span></span> |
| `float3x2& operator-= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="92033-151">Sur place soustrait chaque composant d’une matrice d’une autre matrice.</span><span class="sxs-lookup"><span data-stu-id="92033-151">In-place subtracts each component of a matrix from another matrix.</span></span> |
| `float3x2& operator*= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="92033-152">Sur place, une matrice est multipliée par une autre matrice.</span><span class="sxs-lookup"><span data-stu-id="92033-152">In-place multiplies a matrix by another matrix.</span></span> <span data-ttu-id="92033-153">Cela a pour effet de concaténer deux transformations.</span><span class="sxs-lookup"><span data-stu-id="92033-153">This has the effect of concatenating two transforms.</span></span> |
| `float3x2& operator*= (float3x2& value1, float value2)` | <span data-ttu-id="92033-154">Sur place multiplie chaque composant d’une matrice par une valeur scalaire.</span><span class="sxs-lookup"><span data-stu-id="92033-154">In-place multiplies each component of a matrix by a scalar value.</span></span> |
| `bool operator== (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="92033-155">Détermine si deux instances de float3x2 sont égales.</span><span class="sxs-lookup"><span data-stu-id="92033-155">Determines whether two instances of float3x2 are equal.</span></span> |
| `bool operator!= (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="92033-156">Détermine si deux instances de float3x2 ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="92033-156">Determines whether two instances of float3x2 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2() const` | <span data-ttu-id="92033-157">Convertit un float3x2 en un **Microsoft. Graphics. Canvas. Numerics. Matrix3x2**.</span><span class="sxs-lookup"><span data-stu-id="92033-157">Converts a float3x2 to a **Microsoft.Graphics.Canvas.Numerics.Matrix3x2**.</span></span> |

## <a name="fields"></a><span data-ttu-id="92033-158">Champs</span><span class="sxs-lookup"><span data-stu-id="92033-158">Fields</span></span>

| <span data-ttu-id="92033-159">Nom</span><span class="sxs-lookup"><span data-stu-id="92033-159">Name</span></span> | <span data-ttu-id="92033-160">Description</span><span class="sxs-lookup"><span data-stu-id="92033-160">Description</span></span> |
|-|-|
| `float m11` | <span data-ttu-id="92033-161">Valeur à la ligne 1 colonne 1 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="92033-161">Value at row 1 column 1 of the matrix.</span></span> |
| `float m12` | <span data-ttu-id="92033-162">Valeur à la ligne 1, colonne 2 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="92033-162">Value at row 1 column 2 of the matrix.</span></span> |
| `float m21` | <span data-ttu-id="92033-163">Valeur à la ligne 2 colonne 1 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="92033-163">Value at row 2 column 1 of the matrix.</span></span> |
| `float m22` | <span data-ttu-id="92033-164">Valeur à la ligne 2 colonne 2 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="92033-164">Value at row 2 column 2 of the matrix.</span></span> |
| `float m31` | <span data-ttu-id="92033-165">Valeur à la ligne 3 colonne 1 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="92033-165">Value at row 3 column 1 of the matrix.</span></span> |
| `float m32` | <span data-ttu-id="92033-166">Valeur à la ligne 3 colonne 2 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="92033-166">Value at row 3 column 2 of the matrix.</span></span> |

## <a name="requirements"></a><span data-ttu-id="92033-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92033-167">Requirements</span></span>

| <span data-ttu-id="92033-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92033-168">Requirement</span></span> | <span data-ttu-id="92033-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="92033-169">Value</span></span> |
|-|-|
| <span data-ttu-id="92033-170">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="92033-170">Namespace</span></span> | <span data-ttu-id="92033-171">Windows :: Foundation :: Numerics</span><span class="sxs-lookup"><span data-stu-id="92033-171">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="92033-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="92033-172">Header</span></span> | <dl> <span data-ttu-id="92033-173"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="92033-173"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="92033-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92033-174">See also</span></span>

[<span data-ttu-id="92033-175">API windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="92033-175">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
