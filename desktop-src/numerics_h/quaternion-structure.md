---
title: structure Quaternion (Windowsnumerics. h)
description: Vecteur à quatre dimensions, utilisé pour représenter une rotation.
ms.assetid: A6B25885-8ECB-4039-9DC6-41D5F3A02489
keywords:
- Quaternion, structure
topic_type:
- apiref
api_name:
- quaternion structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ae169232f83e6753505f9d5d07fffac09e67e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537667"
---
# <a name="quaternion-structure"></a><span data-ttu-id="e4410-104">Quaternion, structure</span><span class="sxs-lookup"><span data-stu-id="e4410-104">quaternion Structure</span></span>

<span data-ttu-id="e4410-105">Vecteur à quatre dimensions, utilisé pour représenter une rotation.</span><span class="sxs-lookup"><span data-stu-id="e4410-105">A four dimensional vector, used to represent a rotation.</span></span>

<span data-ttu-id="e4410-106">Un Quaternion peut faire pivoter efficacement un objet autour du vecteur (x, y, z) par le thêta angulaire, où w = cos (thêta/2).</span><span class="sxs-lookup"><span data-stu-id="e4410-106">A quaternion can efficiently rotate an object about the (x, y, z) vector by the angle theta, where w = cos(theta/2).</span></span> <span data-ttu-id="e4410-107">Les quaternions sont généralement utilisés pour l’interpolation lisse entre deux angles, et pour éviter le problème de verrou à cardan qui peut se produire avec des angles Euler.</span><span class="sxs-lookup"><span data-stu-id="e4410-107">Quaternions are typically used for smooth interpolation between two angles, and for avoiding the gimbal lock problem that can occur with Euler angles.</span></span>

<span data-ttu-id="e4410-108">Ce type est disponible uniquement en C++.</span><span class="sxs-lookup"><span data-stu-id="e4410-108">This type is available only in C++.</span></span> <span data-ttu-id="e4410-109">Son équivalent .NET est [System. Numerics. Quaternion](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="e4410-109">Its .NET equivalent is [System.Numerics.Quaternion](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="e4410-110">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="e4410-110">Constructors</span></span>

| <span data-ttu-id="e4410-111">Nom</span><span class="sxs-lookup"><span data-stu-id="e4410-111">Name</span></span> | <span data-ttu-id="e4410-112">Description</span><span class="sxs-lookup"><span data-stu-id="e4410-112">Description</span></span> |
|-|-|
| `quaternion()` | <span data-ttu-id="e4410-113">Crée un Quaternion non initialisé.</span><span class="sxs-lookup"><span data-stu-id="e4410-113">Creates an uninitialized quaternion.</span></span> |
| `quaternion(float x, float y, float z, float w)` | <span data-ttu-id="e4410-114">Crée un Quaternion avec les valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="e4410-114">Creates a quaternion with the specified values.</span></span> |
| `quaternion(float3 vectorPart, float scalarPart)` | <span data-ttu-id="e4410-115">Crée un Quaternion à partir d’un float3 et d’un scalaire.</span><span class="sxs-lookup"><span data-stu-id="e4410-115">Creates a quaternion from a float3 and scalar.</span></span> |
| `quaternion(Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion const& value)` | <span data-ttu-id="e4410-116">Convertit un **Microsoft. Graphics. canevas. Numerics. Quaternion** en un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Quaternion** to a quaternion.</span></span> |

## <a name="functions"></a><span data-ttu-id="e4410-117">Fonctions</span><span class="sxs-lookup"><span data-stu-id="e4410-117">Functions</span></span>

| <span data-ttu-id="e4410-118">Nom</span><span class="sxs-lookup"><span data-stu-id="e4410-118">Name</span></span> | <span data-ttu-id="e4410-119">Description</span><span class="sxs-lookup"><span data-stu-id="e4410-119">Description</span></span> |
|-|-|
| `quaternion make_quaternion_from_axis_angle(float3 const& axis, float angle)` | <span data-ttu-id="e4410-120">Crée un quaternion à partir d'un vecteur et d'un angle de rotation sur le vecteur.</span><span class="sxs-lookup"><span data-stu-id="e4410-120">Creates a quaternion from a vector and an angle to rotate about the vector.</span></span> |
| `quaternion make_quaternion_from_yaw_pitch_roll(float yaw, float pitch, float roll)` | <span data-ttu-id="e4410-121">Crée un Quaternion à partir de l’angle de lacet, du tangage et du roulis spécifiés.</span><span class="sxs-lookup"><span data-stu-id="e4410-121">Creates a quaternion from specified yaw, pitch, and roll angles.</span></span> |
| `quaternion make_quaternion_from_rotation_matrix(float4x4 const& matrix)` | <span data-ttu-id="e4410-122">Crée un Quaternion à partir d’une matrice de rotation.</span><span class="sxs-lookup"><span data-stu-id="e4410-122">Creates a quaternion from a rotation matrix.</span></span> |
| `bool is_identity(quaternion const& value)` | <span data-ttu-id="e4410-123">Vérifie s’il s’agit d’une identité (pas de rotation) Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-123">Checks whether this is an identity (no rotation) quaternion.</span></span> |
| `float length(quaternion const& value)` | <span data-ttu-id="e4410-124">Calcule la longueur d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-124">Calculates the length of a quaternion.</span></span> |
| `float length_squared(quaternion const& value)` | <span data-ttu-id="e4410-125">Calcule la longueur au carré d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-125">Calculates the length squared of a quaternion.</span></span> |
| `float dot(quaternion const& quaternion1, quaternion const& quaternion2)` | <span data-ttu-id="e4410-126">Calcule le produit scalaire de deux quaternions.</span><span class="sxs-lookup"><span data-stu-id="e4410-126">Calculates the dot product of two quaternions.</span></span> |
| `quaternion normalize(quaternion const& value)` | <span data-ttu-id="e4410-127">Divise chaque composant d’un Quaternion par la longueur du Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-127">Divides each component of a quaternion by the length of the quaternion.</span></span> |
| `quaternion conjugate(quaternion const& value)` | <span data-ttu-id="e4410-128">Calcule le conjugué d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-128">Calculates the conjugate of a quaternion.</span></span> |
| `quaternion inverse(quaternion const& value)` | <span data-ttu-id="e4410-129">Calcule l’inverse d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-129">Calculates the inverse of a quaternion.</span></span> |
| `quaternion slerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | <span data-ttu-id="e4410-130">Effectue une interpolation entre deux quaternions, en utilisant une interpolation linéaire sphérique.</span><span class="sxs-lookup"><span data-stu-id="e4410-130">Interpolates between two quaternions, using spherical linear interpolation.</span></span> |
| `quaternion lerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | <span data-ttu-id="e4410-131">Interpole de manière linéaire entre deux quaternions.</span><span class="sxs-lookup"><span data-stu-id="e4410-131">Linearly interpolates between two quaternions.</span></span> |
| `quaternion concatenate(quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="e4410-132">Concatène deux quaternions ; le résultat représente la première rotation suivie de la deuxième rotation.</span><span class="sxs-lookup"><span data-stu-id="e4410-132">Concatenates two quaternions; the result represents the first rotation followed by the second rotation.</span></span> |

## <a name="methods"></a><span data-ttu-id="e4410-133">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e4410-133">Methods</span></span>

| <span data-ttu-id="e4410-134">Nom</span><span class="sxs-lookup"><span data-stu-id="e4410-134">Name</span></span> | <span data-ttu-id="e4410-135">Description</span><span class="sxs-lookup"><span data-stu-id="e4410-135">Description</span></span> |
|-|-|
| `static quaternion identity()` | <span data-ttu-id="e4410-136">Retourne une instance du Quaternion d’identité.</span><span class="sxs-lookup"><span data-stu-id="e4410-136">Returns an instance of the identity quaternion.</span></span> |

## <a name="operators"></a><span data-ttu-id="e4410-137">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="e4410-137">Operators</span></span>

| <span data-ttu-id="e4410-138">Nom</span><span class="sxs-lookup"><span data-stu-id="e4410-138">Name</span></span> | <span data-ttu-id="e4410-139">Description</span><span class="sxs-lookup"><span data-stu-id="e4410-139">Description</span></span> |
|-|-|
| `quaternion operator+ (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="e4410-140">Ajoute deux quaternions.</span><span class="sxs-lookup"><span data-stu-id="e4410-140">Adds two quaternions.</span></span> |
| `quaternion operator- (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="e4410-141">Soustrait un Quaternion d’un autre Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-141">Subtracts a quaternion from another quaternion.</span></span> |
| `quaternion operator* (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="e4410-142">Multiplie un Quaternion par un autre Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-142">Multiplies a quaternion by another quaternion.</span></span> |
| `quaternion operator* (quaternion const& value1, float value2)` | <span data-ttu-id="e4410-143">Multiplie un Quaternion par une valeur scalaire.</span><span class="sxs-lookup"><span data-stu-id="e4410-143">Multiplies a quaternion by a scalar value.</span></span> |
| `quaternion operator/ (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="e4410-144">Divise un Quaternion par un autre Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-144">Divides a quaternion by another quaternion.</span></span> |
| `quaternion operator- (quaternion const& value)` | <span data-ttu-id="e4410-145">Retourne le signe de chaque composant du Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-145">Flips the sign of each component of the quaternion.</span></span> |
| `quaternion& operator+= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="e4410-146">Sur place ajoute deux quaternions.</span><span class="sxs-lookup"><span data-stu-id="e4410-146">In-place adds two quaternions.</span></span> |
| `quaternion& operator-= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="e4410-147">Sur place soustrait un Quaternion d’un autre Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-147">In-place subtracts a quaternion from another quaternion.</span></span> |
| `quaternion& operator*= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="e4410-148">Sur place, multiplie un Quaternion par un autre Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-148">In-place multiplies a quaternion by another quaternion.</span></span> |
| `quaternion& operator*= (quaternion& value1, float value2)` | <span data-ttu-id="e4410-149">Nultiplies sur place un Quaternion par une valeur scalaire.</span><span class="sxs-lookup"><span data-stu-id="e4410-149">In-place nultiplies a quaternion by a scalar value.</span></span> |
| `quaternion& operator/= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="e4410-150">Sur place, divise un Quaternion par un autre Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-150">In-place divides a quaternion by another quaternion.</span></span> |
| `bool operator== (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="e4410-151">Détermine si deux instances de Quaternion sont égales.</span><span class="sxs-lookup"><span data-stu-id="e4410-151">Determines whether two instances of quaternion are equal.</span></span> |
| `bool operator!= (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="e4410-152">Détermine si deux instances de Quaternion ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="e4410-152">Determines whether two instances of quaternion are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion() const` | <span data-ttu-id="e4410-153">Convertit un quaternion en un **Microsoft. Graphics. canevas. Numerics. Quaternion**.</span><span class="sxs-lookup"><span data-stu-id="e4410-153">Converts a quaternion to a **Microsoft.Graphics.Canvas.Numerics.Quaternion**.</span></span> |

## <a name="fields"></a><span data-ttu-id="e4410-154">Champs</span><span class="sxs-lookup"><span data-stu-id="e4410-154">Fields</span></span>

| <span data-ttu-id="e4410-155">Nom</span><span class="sxs-lookup"><span data-stu-id="e4410-155">Name</span></span> | <span data-ttu-id="e4410-156">Description</span><span class="sxs-lookup"><span data-stu-id="e4410-156">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="e4410-157">Valeur X du composant vecteur du Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-157">X value of the vector component of the quaternion.</span></span> |
| `float y` | <span data-ttu-id="e4410-158">Valeur Y du composant vecteur du Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-158">Y value of the vector component of the quaternion.</span></span> |
| `float z` | <span data-ttu-id="e4410-159">Valeur Z du composant vecteur du Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-159">Z value of the vector component of the quaternion.</span></span> |
| `float w` | <span data-ttu-id="e4410-160">Composant de rotation du Quaternion.</span><span class="sxs-lookup"><span data-stu-id="e4410-160">Rotation component of the quaternion.</span></span> |

## <a name="requirements"></a><span data-ttu-id="e4410-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4410-161">Requirements</span></span>

| <span data-ttu-id="e4410-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4410-162">Requirement</span></span> | <span data-ttu-id="e4410-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4410-163">Value</span></span> |
|-|-|
| <span data-ttu-id="e4410-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e4410-164">Namespace</span></span> | <span data-ttu-id="e4410-165">Windows :: Foundation :: Numerics</span><span class="sxs-lookup"><span data-stu-id="e4410-165">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="e4410-166">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4410-166">Header</span></span> | <dl> <span data-ttu-id="e4410-167"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4410-167"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="e4410-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4410-168">See also</span></span>

[<span data-ttu-id="e4410-169">API windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="e4410-169">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
