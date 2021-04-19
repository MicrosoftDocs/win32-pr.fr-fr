---
title: float4x4, structure (Windowsnumerics. h)
description: Matrice 4x4, utilisée pour les transformations 3D.
ms.assetid: C0D2198A-B547-4153-AD02-9A47835FD272
keywords:
- float4x4, structure
topic_type:
- apiref
api_name:
- float4x4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71c91de5eef404db33eff118568540be912d551d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535019"
---
# <a name="float4x4-structure"></a><span data-ttu-id="7ae97-104">float4x4, structure</span><span class="sxs-lookup"><span data-stu-id="7ae97-104">float4x4 structure</span></span>

<span data-ttu-id="7ae97-105">Matrice 4x4, utilisée pour les transformations 3D.</span><span class="sxs-lookup"><span data-stu-id="7ae97-105">A 4x4 matrix, used for 3D transforms.</span></span>

<span data-ttu-id="7ae97-106">Ce type de matrice utilise une disposition de vecteur de ligne.</span><span class="sxs-lookup"><span data-stu-id="7ae97-106">This matrix type uses a row vector layout.</span></span> <span data-ttu-id="7ae97-107">Les coordonnées x, y et z du vecteur de translation de cette matrice correspondent aux champs M41, M42, M43.</span><span class="sxs-lookup"><span data-stu-id="7ae97-107">The x, y, and z of this matrix's translation vector correspond to the fields m41, m42, m43.</span></span>

<span data-ttu-id="7ae97-108">Ce type est disponible uniquement en C++.</span><span class="sxs-lookup"><span data-stu-id="7ae97-108">This type is available only in C++.</span></span> <span data-ttu-id="7ae97-109">Son équivalent .NET est [System. Numerics. Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="7ae97-109">Its .NET equivalent is [System.Numerics.Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="7ae97-110">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="7ae97-110">Constructors</span></span>

| <span data-ttu-id="7ae97-111">Nom</span><span class="sxs-lookup"><span data-stu-id="7ae97-111">Name</span></span> | <span data-ttu-id="7ae97-112">Description</span><span class="sxs-lookup"><span data-stu-id="7ae97-112">Description</span></span> |
|-|-|
| `float4x4()` | <span data-ttu-id="7ae97-113">Crée un float4x4 non initialisé.</span><span class="sxs-lookup"><span data-stu-id="7ae97-113">Creates an uninitialized float4x4.</span></span> |
| `float4x4(float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34, float m41, float m42, float m43, float m44)` | <span data-ttu-id="7ae97-114">Crée un float4x4 avec les valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="7ae97-114">Creates a float4x4 with the specified values.</span></span> |
| `explicit float4x4(float3x2 value)` | <span data-ttu-id="7ae97-115">Crée un float4x4 à partir d’un float3x2.</span><span class="sxs-lookup"><span data-stu-id="7ae97-115">Creates a float4x4 from a float3x2.</span></span> |
| `float4x4(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4 const& value)` | <span data-ttu-id="7ae97-116">Convertit un **Microsoft. Graphics. canevas. Numerics. Matrix4x4** en float4x4.</span><span class="sxs-lookup"><span data-stu-id="7ae97-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Matrix4x4** to a float4x4.</span></span> |

## <a name="functions"></a><span data-ttu-id="7ae97-117">Fonctions</span><span class="sxs-lookup"><span data-stu-id="7ae97-117">Functions</span></span>

| <span data-ttu-id="7ae97-118">Nom</span><span class="sxs-lookup"><span data-stu-id="7ae97-118">Name</span></span> | <span data-ttu-id="7ae97-119">Description</span><span class="sxs-lookup"><span data-stu-id="7ae97-119">Description</span></span> |
|-|-|
| `float4x4 make_float4x4_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& cameraUpVector, float3 const& cameraForwardVector)` | <span data-ttu-id="7ae97-120">Crée un panneau sphérique qui pivote autour de la position d’un objet spécifié, à l’aide d’un système de coordonnées droitier.</span><span class="sxs-lookup"><span data-stu-id="7ae97-120">Creates a spherical billboard that rotates around a specified object position, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?constrained_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& rotateAxis, float3 const& cameraForwardVector, float3 const& objectForwardVector)` | <span data-ttu-id="7ae97-121">Crée un panneau cylindrique qui pivote autour d’un axe spécifié, à l’aide d’un système de coordonnées droitier.</span><span class="sxs-lookup"><span data-stu-id="7ae97-121">Creates a cylindrical billboard that rotates around a specified axis, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_translation(float3 const& position)` | <span data-ttu-id="7ae97-122">Crée une matrice de translation.</span><span class="sxs-lookup"><span data-stu-id="7ae97-122">Creates a translation matrix.</span></span> |
| `float4x4 make_float4x4_translation(float xPosition, float yPosition, float zPosition)` | <span data-ttu-id="7ae97-123">Crée une matrice de translation.</span><span class="sxs-lookup"><span data-stu-id="7ae97-123">Creates a translation matrix.</span></span> |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale)` | <span data-ttu-id="7ae97-124">Crée une matrice de mise à l’échelle, centrée sur l’origine.</span><span class="sxs-lookup"><span data-stu-id="7ae97-124">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale, float3 const& centerPoint)` | <span data-ttu-id="7ae97-125">Crée une matrice de mise à l’échelle, centrée sur le point spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ae97-125">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_scale(float3 const& scales)` | <span data-ttu-id="7ae97-126">Crée une matrice de mise à l’échelle, centrée sur l’origine.</span><span class="sxs-lookup"><span data-stu-id="7ae97-126">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float3 const& scales, float3 const& centerPoint)` | <span data-ttu-id="7ae97-127">Crée une matrice de mise à l’échelle, centrée sur le point spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ae97-127">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_scale(float scale)` | <span data-ttu-id="7ae97-128">Crée une matrice de mise à l’échelle, centrée sur l’origine.</span><span class="sxs-lookup"><span data-stu-id="7ae97-128">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float scale, float3 const& centerPoint)` | <span data-ttu-id="7ae97-129">Crée une matrice de mise à l’échelle, centrée sur le point spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ae97-129">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_x(float radians)` | <span data-ttu-id="7ae97-130">Crée une matrice de rotation de l’axe x, centrée sur l’origine.</span><span class="sxs-lookup"><span data-stu-id="7ae97-130">Creates an x-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_x(float radians, float3 const& centerPoint)` | <span data-ttu-id="7ae97-131">Crée une matrice de rotation de l’axe des x, centrée sur le point spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ae97-131">Creates an x-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_y(float radians)` | <span data-ttu-id="7ae97-132">Crée une matrice de rotation de l’axe y, centrée sur l’origine.</span><span class="sxs-lookup"><span data-stu-id="7ae97-132">Creates a y-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_y(float radians, float3 const& centerPoint)` | <span data-ttu-id="7ae97-133">Crée une matrice de rotation de l’axe y, centrée sur le point spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ae97-133">Creates a y-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_z(float radians)` | <span data-ttu-id="7ae97-134">Crée une matrice de rotation de l’axe z, centrée sur l’origine.</span><span class="sxs-lookup"><span data-stu-id="7ae97-134">Creates a z-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_z(float radians, float3 const& centerPoint)` | <span data-ttu-id="7ae97-135">Crée une matrice de rotation de l’axe z, centrée sur le point spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ae97-135">Creates a z-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_from_axis_angle(float3 const& axis, float angle)` | <span data-ttu-id="7ae97-136">Crée une matrice qui pivote autour d'un vecteur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="7ae97-136">Creates a matrix that rotates around an arbitrary vector.</span></span> |
| `float4x4 make_float4x4_?perspective_field_of_view(float fieldOfView, float aspectRatio, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="7ae97-137">Crée une matrice de projection de perspective basée sur un champ de vue, à l’aide d’un système de coordonnées droitier.</span><span class="sxs-lookup"><span data-stu-id="7ae97-137">Creates a perspective projection matrix based on a field of view, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_perspective(float width, float height, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="7ae97-138">Crée une matrice de projection de perspective à l’aide d’un système de coordonnées droitier.</span><span class="sxs-lookup"><span data-stu-id="7ae97-138">Creates a perspective projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?perspective_off_center(float left, float right, float bottom, float top, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="7ae97-139">Crée une matrice de projection de perspective personnalisée, à l’aide d’un système de coordonnées droitier.</span><span class="sxs-lookup"><span data-stu-id="7ae97-139">Creates a customized perspective projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_orthographic(float width, float height, float zNearPlane, float zFarPlane)` | <span data-ttu-id="7ae97-140">Crée une matrice de projection orthographique à l’aide d’un système de coordonnées droitier.</span><span class="sxs-lookup"><span data-stu-id="7ae97-140">Creates an orthographic projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?orthographic_off_center(float left, float right, float bottom, float top, float zNearPlane, float zFarPlane)` | <span data-ttu-id="7ae97-141">Crée une matrice de projection orthographique personnalisée, à l’aide d’un système de coordonnées droitier.</span><span class="sxs-lookup"><span data-stu-id="7ae97-141">Creates a customized orthographic projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_look_at(float3 const& cameraPosition, float3 const& cameraTarget, float3 const& cameraUpVector)` | <span data-ttu-id="7ae97-142">Crée une matrice de vue à l’aide d’un système de coordonnées droitier.</span><span class="sxs-lookup"><span data-stu-id="7ae97-142">Creates a view matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_world(float3 const& position, float3 const& forward, float3 const& up)` | <span data-ttu-id="7ae97-143">Crée une matrice universelle à l’aide d’un système de coordonnées droitier.</span><span class="sxs-lookup"><span data-stu-id="7ae97-143">Creates a world matrix, using a right handed coordinate system.</span></span> <span data-ttu-id="7ae97-144">Cela peut être utilisé pour positionner des objets dans l’espace 3D.</span><span class="sxs-lookup"><span data-stu-id="7ae97-144">This can be used to position objects in 3D space.</span></span> |
| `float4x4 make_float4x4_?from_quaternion(quaternion const& quaternion)` | <span data-ttu-id="7ae97-145">Crée une matrice de rotation à partir d’un Quaternion.</span><span class="sxs-lookup"><span data-stu-id="7ae97-145">Creates a rotation matrix from a quaternion.</span></span> |
| `float4x4 make_float4x4_?from_yaw_pitch_roll(float yaw, float pitch, float roll)` | <span data-ttu-id="7ae97-146">Crée une matrice de rotation à partir d’un lacet, du tangage et du roulis spécifiés.</span><span class="sxs-lookup"><span data-stu-id="7ae97-146">Creates a rotation matrix from a specified yaw, pitch, and roll.</span></span> |
| `float4x4 make_float4x4_shadow(float3 const& lightDirection, plane const& plane)` | <span data-ttu-id="7ae97-147">Crée une matrice qui aplanit la géométrie dans un plan spécifié en la faisant correspondre à une ombre provenant d'une source de lumière spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7ae97-147">Creates a matrix that flattens geometry into a specified plane as if casting a shadow from a specified light source.</span></span> |
| `float4x4 make_float4x4_reflection(plane const& value)` | <span data-ttu-id="7ae97-148">Crée une matrice qui reflète le système de coordonnées pour un plan spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ae97-148">Creates a matrix that reflects the coordinate system about a specified plane.</span></span> |
| `bool is_identity(float4x4 const& value)` | <span data-ttu-id="7ae97-149">Vérifie s’il s’agit d’une matrice d’identité.</span><span class="sxs-lookup"><span data-stu-id="7ae97-149">Checks whether this is an identity matrix.</span></span> |
| `float determinant(float4x4 const& value)` | <span data-ttu-id="7ae97-150">Calcule le déterminant de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-150">Calculates the determinant of the matrix.</span></span> |
| `float3 translation(float4x4 const& value)` | <span data-ttu-id="7ae97-151">Obtient le vecteur de translation de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-151">Gets the translation vector of the matrix.</span></span> |
| `bool invert(float4x4 const& matrix, _Out_ float4x4* result)` | <span data-ttu-id="7ae97-152">Calcule l’inverse d’une matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-152">Calculates the inverse of a matrix.</span></span> <span data-ttu-id="7ae97-153">Retourne la valeur true si la matrice peut être inversée ; false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7ae97-153">Returns true if the matrix can be inverted; false otherwise.</span></span> |
| `bool decompose(float4x4 const& matrix, _Out_ float3* scale, _Out_ quaternion* rotation, _Out_ float3* translation)` | <span data-ttu-id="7ae97-154">Extrait les composants scalaires, de translation et de rotation à partir d’une matrice de mise à l’échelle/rotation/translation (SRT) 3D.</span><span class="sxs-lookup"><span data-stu-id="7ae97-154">Extracts the scalar, translation, and rotation components from a 3D scale/rotate/translate (SRT) matrix.</span></span> <span data-ttu-id="7ae97-155">Retourne la valeur true si la matrice peut être décomposée ; false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7ae97-155">Returns true if the matrix can be decomposed; false otherwise.</span></span> |
| `float4x4 transform(float4x4 const& value, quaternion const& rotation)` | <span data-ttu-id="7ae97-156">Transforme une matrice en appliquant une rotation de Quaternion.</span><span class="sxs-lookup"><span data-stu-id="7ae97-156">Transforms a matrix by applying a quaternion rotation.</span></span> |
| `float4x4 transpose(float4x4 const& matrix)` | <span data-ttu-id="7ae97-157">Transpose les composants d’une matrice le long de la diagonale.</span><span class="sxs-lookup"><span data-stu-id="7ae97-157">Transposes the components of a matrix along its diagonal.</span></span> |
| `float4x4 lerp(float4x4 const& matrix1, float4x4 const& matrix2, float amount)` | <span data-ttu-id="7ae97-158">Interpole de manière linéaire entre les valeurs correspondantes de deux matrices.</span><span class="sxs-lookup"><span data-stu-id="7ae97-158">Linearly interpolates between the corresponding values of two matrices.</span></span> |

## <a name="methods"></a><span data-ttu-id="7ae97-159">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7ae97-159">Methods</span></span>

| <span data-ttu-id="7ae97-160">Nom</span><span class="sxs-lookup"><span data-stu-id="7ae97-160">Name</span></span> | <span data-ttu-id="7ae97-161">Description</span><span class="sxs-lookup"><span data-stu-id="7ae97-161">Description</span></span> |
|-|-|
| `static float4x4 identity()` | <span data-ttu-id="7ae97-162">Retourne une instance de la matrice d’identité.</span><span class="sxs-lookup"><span data-stu-id="7ae97-162">Returns an instance of the identity matrix.</span></span> |

## <a name="operators"></a><span data-ttu-id="7ae97-163">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="7ae97-163">Operators</span></span>

| <span data-ttu-id="7ae97-164">Nom</span><span class="sxs-lookup"><span data-stu-id="7ae97-164">Name</span></span> | <span data-ttu-id="7ae97-165">Description</span><span class="sxs-lookup"><span data-stu-id="7ae97-165">Description</span></span> |
|-|-|
| `float4x4 operator+ (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="7ae97-166">Ajoute chaque composant d’une matrice à une autre matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-166">Adds each component of a matrix to another matrix.</span></span> |
| `float4x4 operator- (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="7ae97-167">Soustrait chaque composant d’une matrice d’une autre matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-167">Subtracts each component of a matrix from another matrix.</span></span> |
| `float4x4 operator* (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="7ae97-168">Multiplie une matrice par une autre matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-168">Multiplies a matrix by another matrix.</span></span> <span data-ttu-id="7ae97-169">Cela a pour effet de concaténer deux transformations.</span><span class="sxs-lookup"><span data-stu-id="7ae97-169">This has the effect of concatenating two transforms.</span></span> |
| `float4x4 operator* (float4x4 const& value1, float value2)` | <span data-ttu-id="7ae97-170">Multiplie chaque composant d’une matrice par une valeur scalaire.</span><span class="sxs-lookup"><span data-stu-id="7ae97-170">Multiplies each component of a matrix by a scalar value.</span></span> |
| `float4x4 operator- (float4x4 const& value)` | <span data-ttu-id="7ae97-171">Nie chaque composant d’une matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-171">Negates each component of a matrix.</span></span> |
| `float4x4& operator+= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="7ae97-172">Sur place ajoute chaque composant d’une matrice à une autre matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-172">In-place adds each component of a matrix to another matrix.</span></span> |
| `float4x4& operator-= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="7ae97-173">Sur place soustrait chaque composant d’une matrice d’une autre matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-173">In-place subtracts each component of a matrix from another matrix.</span></span> |
| `float4x4& operator*= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="7ae97-174">Sur place, une matrice est multipliée par une autre matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-174">In-place multiplies a matrix by another matrix.</span></span> <span data-ttu-id="7ae97-175">Cela a pour effet de concaténer deux transformations.</span><span class="sxs-lookup"><span data-stu-id="7ae97-175">This has the effect of concatenating two transforms.</span></span> |
| `float4x4& operator*= (float4x4& value1, float value2)` | <span data-ttu-id="7ae97-176">Sur place multiplie chaque composant d’une matrice par une valeur scalaire.</span><span class="sxs-lookup"><span data-stu-id="7ae97-176">In-place multiplies each component of a matrix by a scalar value.</span></span> |
| `bool operator== (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="7ae97-177">Détermine si deux instances de float4x4 sont égales.</span><span class="sxs-lookup"><span data-stu-id="7ae97-177">Determines whether two instances of float4x4 are equal.</span></span> |
| `bool operator!= (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="7ae97-178">Détermine si deux instances de float4x4 ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="7ae97-178">Determines whether two instances of float4x4 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4() const` | <span data-ttu-id="7ae97-179">Convertit un float4x4 en un **Microsoft. Graphics. Canvas. Numerics. Matrix4x4**.</span><span class="sxs-lookup"><span data-stu-id="7ae97-179">Converts a float4x4 to a **Microsoft.Graphics.Canvas.Numerics.Matrix4x4**.</span></span> |

## <a name="fields"></a><span data-ttu-id="7ae97-180">Champs</span><span class="sxs-lookup"><span data-stu-id="7ae97-180">Fields</span></span>

| <span data-ttu-id="7ae97-181">Nom</span><span class="sxs-lookup"><span data-stu-id="7ae97-181">Name</span></span> | <span data-ttu-id="7ae97-182">Description</span><span class="sxs-lookup"><span data-stu-id="7ae97-182">Description</span></span> |
|-|-|
| `float m11` | <span data-ttu-id="7ae97-183">Valeur à la ligne 1 colonne 1 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-183">Value at row 1 column 1 of the matrix.</span></span> |
| `float m12` | <span data-ttu-id="7ae97-184">Valeur à la ligne 1, colonne 2 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-184">Value at row 1 column 2 of the matrix.</span></span> |
| `float m13` | <span data-ttu-id="7ae97-185">Valeur à la ligne 1 colonne 3 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-185">Value at row 1 column 3 of the matrix.</span></span> |
| `float m14` | <span data-ttu-id="7ae97-186">Valeur à la ligne 1 colonne 4 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-186">Value at row 1 column 4 of the matrix.</span></span> |
| `float m21` | <span data-ttu-id="7ae97-187">Valeur à la ligne 2 colonne 1 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-187">Value at row 2 column 1 of the matrix.</span></span> |
| `float m22` | <span data-ttu-id="7ae97-188">Valeur à la ligne 2 colonne 2 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-188">Value at row 2 column 2 of the matrix.</span></span> |
| `float m23` | <span data-ttu-id="7ae97-189">Valeur à la ligne 2, colonne 3 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-189">Value at row 2 column 3 of the matrix.</span></span> |
| `float m24` | <span data-ttu-id="7ae97-190">Valeur à la ligne 2 colonne 4 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-190">Value at row 2 column 4 of the matrix.</span></span> |
| `float m31` | <span data-ttu-id="7ae97-191">Valeur à la ligne 3 colonne 1 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-191">Value at row 3 column 1 of the matrix.</span></span> |
| `float m32` | <span data-ttu-id="7ae97-192">Valeur à la ligne 3 colonne 2 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-192">Value at row 3 column 2 of the matrix.</span></span> |
| `float m33` | <span data-ttu-id="7ae97-193">Valeur à la ligne 3 colonne 3 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-193">Value at row 3 column 3 of the matrix.</span></span> |
| `float m34` | <span data-ttu-id="7ae97-194">Valeur à la ligne 3 colonne 4 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-194">Value at row 3 column 4 of the matrix.</span></span> |
| `float m41` | <span data-ttu-id="7ae97-195">Valeur à la ligne 4 colonne 1 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-195">Value at row 4 column 1 of the matrix.</span></span> |
| `float m42` | <span data-ttu-id="7ae97-196">Valeur à la ligne 4 colonne 2 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-196">Value at row 4 column 2 of the matrix.</span></span> |
| `float m43` | <span data-ttu-id="7ae97-197">Valeur à la ligne 4 colonne 3 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-197">Value at row 4 column 3 of the matrix.</span></span> |
| `float m44` | <span data-ttu-id="7ae97-198">Valeur à la ligne 4 colonne 4 de la matrice.</span><span class="sxs-lookup"><span data-stu-id="7ae97-198">Value at row 4 column 4 of the matrix.</span></span> |

## <a name="requirements"></a><span data-ttu-id="7ae97-199">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ae97-199">Requirements</span></span>

| <span data-ttu-id="7ae97-200">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ae97-200">Requirement</span></span> | <span data-ttu-id="7ae97-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ae97-201">Value</span></span> |
|-|-|
| <span data-ttu-id="7ae97-202">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7ae97-202">Namespace</span></span> | <span data-ttu-id="7ae97-203">Windows :: Foundation :: Numerics</span><span class="sxs-lookup"><span data-stu-id="7ae97-203">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="7ae97-204">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ae97-204">Header</span></span> | <dl> <span data-ttu-id="7ae97-205"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ae97-205"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="7ae97-206">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ae97-206">See also</span></span>

[<span data-ttu-id="7ae97-207">API windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="7ae97-207">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
