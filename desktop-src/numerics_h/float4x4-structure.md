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
ms.openlocfilehash: 549c9328dad3bb04c7e4a46ead6a1aedbe04cfe6
ms.sourcegitcommit: 8a211d404470a6a2790733ed2894cfaf92bddd70
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2021
ms.locfileid: "123464123"
---
# <a name="float4x4-structure"></a>float4x4, structure

Matrice 4x4, utilisée pour les transformations 3D.

Ce type de matrice utilise une disposition de vecteur de ligne. Les coordonnées x, y et z du vecteur de translation de cette matrice correspondent aux champs M41, M42, M43.

Ce type est disponible uniquement en C++. Son équivalent .NET est [System. Numerics. Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8).

## <a name="constructors"></a>Constructeurs

| Nom | Description |
|-|-|
| `float4x4()` | Crée un float4x4 non initialisé. |
| `float4x4(float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34, float m41, float m42, float m43, float m44)` | Crée un float4x4 avec les valeurs spécifiées. |
| `explicit float4x4(float3x2 value)` | Crée un float4x4 à partir d’un float3x2. |
| `float4x4(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4 const& value)` | Convertit un **Microsoft. Graphics. canevas. Numerics. Matrix4x4** en float4x4. |

## <a name="functions"></a>Fonctions

| Name | Description |
|-|-|
| `float4x4 make_float4x4_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& cameraUpVector, float3 const& cameraForwardVector)` | Crée un panneau sphérique qui pivote autour de la position d’un objet spécifié, à l’aide d’un système de coordonnées droitier. |
| `float4x4 make_float4x4_?constrained_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& rotateAxis, float3 const& cameraForwardVector, float3 const& objectForwardVector)` | Crée un panneau cylindrique qui pivote autour d’un axe spécifié, à l’aide d’un système de coordonnées droitier. |
| `float4x4 make_float4x4_translation(float3 const& position)` | Crée une matrice de translation. |
| `float4x4 make_float4x4_translation(float xPosition, float yPosition, float zPosition)` | Crée une matrice de translation. |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale)` | Crée une matrice de mise à l’échelle, centrée sur l’origine. |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale, float3 const& centerPoint)` | Crée une matrice de mise à l’échelle, centrée sur le point spécifié. |
| `float4x4 make_float4x4_scale(float3 const& scales)` | Crée une matrice de mise à l’échelle, centrée sur l’origine. |
| `float4x4 make_float4x4_scale(float3 const& scales, float3 const& centerPoint)` | Crée une matrice de mise à l’échelle, centrée sur le point spécifié. |
| `float4x4 make_float4x4_scale(float scale)` | Crée une matrice de mise à l’échelle, centrée sur l’origine. |
| `float4x4 make_float4x4_scale(float scale, float3 const& centerPoint)` | Crée une matrice de mise à l’échelle, centrée sur le point spécifié. |
| `float4x4 make_float4x4_rotation_x(float radians)` | Crée une matrice de rotation de l’axe x, centrée sur l’origine. |
| `float4x4 make_float4x4_rotation_x(float radians, float3 const& centerPoint)` | Crée une matrice de rotation de l’axe des x, centrée sur le point spécifié. |
| `float4x4 make_float4x4_rotation_y(float radians)` | Crée une matrice de rotation de l’axe y, centrée sur l’origine. |
| `float4x4 make_float4x4_rotation_y(float radians, float3 const& centerPoint)` | Crée une matrice de rotation de l’axe y, centrée sur le point spécifié. |
| `float4x4 make_float4x4_rotation_z(float radians)` | Crée une matrice de rotation de l’axe z, centrée sur l’origine. |
| `float4x4 make_float4x4_rotation_z(float radians, float3 const& centerPoint)` | Crée une matrice de rotation de l’axe z, centrée sur le point spécifié. |
| `float4x4 make_float4x4_from_axis_angle(float3 const& axis, float angle)` | Crée une matrice qui pivote autour d'un vecteur arbitraire. |
| `float4x4 make_float4x4_perspective_field_of_view(float fieldOfView, float aspectRatio, float nearPlaneDistance, float farPlaneDistance)` | Crée une matrice de projection de perspective basée sur un champ de vue, à l’aide d’un système de coordonnées droitier. |
| `float4x4 make_float4x4_perspective(float width, float height, float nearPlaneDistance, float farPlaneDistance)` | Crée une matrice de projection de perspective à l’aide d’un système de coordonnées droitier. |
| `float4x4 make_float4x4_perspective_off_center(float left, float right, float bottom, float top, float nearPlaneDistance, float farPlaneDistance)` | Crée une matrice de projection de perspective personnalisée, à l’aide d’un système de coordonnées droitier. |
| `float4x4 make_float4x4_orthographic(float width, float height, float zNearPlane, float zFarPlane)` | Crée une matrice de projection orthographique à l’aide d’un système de coordonnées droitier. |
| `float4x4 make_float4x4_?orthographic_off_center(float left, float right, float bottom, float top, float zNearPlane, float zFarPlane)` | Crée une matrice de projection orthographique personnalisée, à l’aide d’un système de coordonnées droitier. |
| `float4x4 make_float4x4_look_at(float3 const& cameraPosition, float3 const& cameraTarget, float3 const& cameraUpVector)` | Crée une matrice de vue à l’aide d’un système de coordonnées droitier. |
| `float4x4 make_float4x4_world(float3 const& position, float3 const& forward, float3 const& up)` | Crée une matrice universelle à l’aide d’un système de coordonnées droitier. Cela peut être utilisé pour positionner des objets dans l’espace 3D. |
| `float4x4 make_float4x4_from_quaternion(quaternion const& quaternion)` | Crée une matrice de rotation à partir d’un Quaternion. |
| `float4x4 make_float4x4_from_yaw_pitch_roll(float yaw, float pitch, float roll)` | Crée une matrice de rotation à partir d’un lacet, du tangage et du roulis spécifiés. |
| `float4x4 make_float4x4_shadow(float3 const& lightDirection, plane const& plane)` | Crée une matrice qui aplanit la géométrie dans un plan spécifié en la faisant correspondre à une ombre provenant d'une source de lumière spécifiée. |
| `float4x4 make_float4x4_reflection(plane const& value)` | Crée une matrice qui reflète le système de coordonnées pour un plan spécifié. |
| `bool is_identity(float4x4 const& value)` | Vérifie s’il s’agit d’une matrice d’identité. |
| `float determinant(float4x4 const& value)` | Calcule le déterminant de la matrice. |
| `float3 translation(float4x4 const& value)` | Obtient le vecteur de translation de la matrice. |
| `bool invert(float4x4 const& matrix, _Out_ float4x4* result)` | Calcule l’inverse d’une matrice. Retourne la valeur true si la matrice peut être inversée ; false dans le cas contraire. |
| `bool decompose(float4x4 const& matrix, _Out_ float3* scale, _Out_ quaternion* rotation, _Out_ float3* translation)` | Extrait les composants scalaires, de translation et de rotation à partir d’une matrice de mise à l’échelle/rotation/translation (SRT) 3D. Retourne la valeur true si la matrice peut être décomposée ; false dans le cas contraire. |
| `float4x4 transform(float4x4 const& value, quaternion const& rotation)` | Transforme une matrice en appliquant une rotation de Quaternion. |
| `float4x4 transpose(float4x4 const& matrix)` | Transpose les composants d’une matrice le long de la diagonale. |
| `float4x4 lerp(float4x4 const& matrix1, float4x4 const& matrix2, float amount)` | Interpole de manière linéaire entre les valeurs correspondantes de deux matrices. |

## <a name="methods"></a>Méthodes

| Nom | Description |
|-|-|
| `static float4x4 identity()` | Retourne une instance de la matrice d’identité. |

## <a name="operators"></a>Opérateurs

| Name | Description |
|-|-|
| `float4x4 operator+ (float4x4 const& value1, float4x4 const& value2)` | Ajoute chaque composant d’une matrice à une autre matrice. |
| `float4x4 operator- (float4x4 const& value1, float4x4 const& value2)` | Soustrait chaque composant d’une matrice d’une autre matrice. |
| `float4x4 operator* (float4x4 const& value1, float4x4 const& value2)` | Multiplie une matrice par une autre matrice. Cela a pour effet de concaténer deux transformations. |
| `float4x4 operator* (float4x4 const& value1, float value2)` | Multiplie chaque composant d’une matrice par une valeur scalaire. |
| `float4x4 operator- (float4x4 const& value)` | Nie chaque composant d’une matrice. |
| `float4x4& operator+= (float4x4& value1, float4x4 const& value2)` | Sur place ajoute chaque composant d’une matrice à une autre matrice. |
| `float4x4& operator-= (float4x4& value1, float4x4 const& value2)` | Sur place soustrait chaque composant d’une matrice d’une autre matrice. |
| `float4x4& operator*= (float4x4& value1, float4x4 const& value2)` | Sur place, une matrice est multipliée par une autre matrice. Cela a pour effet de concaténer deux transformations. |
| `float4x4& operator*= (float4x4& value1, float value2)` | Sur place multiplie chaque composant d’une matrice par une valeur scalaire. |
| `bool operator== (float4x4 const& value1, float4x4 const& value2)` | Détermine si deux instances de float4x4 sont égales. |
| `bool operator!= (float4x4 const& value1, float4x4 const& value2)` | Détermine si deux instances de float4x4 ne sont pas égales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4() const` | Convertit un float4x4 en un **Microsoft. Graphics. Canvas. Numerics. Matrix4x4**. |

## <a name="fields"></a>Champs

| Nom | Description |
|-|-|
| `float m11` | Valeur à la ligne 1 colonne 1 de la matrice. |
| `float m12` | Valeur à la ligne 1, colonne 2 de la matrice. |
| `float m13` | Valeur à la ligne 1 colonne 3 de la matrice. |
| `float m14` | Valeur à la ligne 1 colonne 4 de la matrice. |
| `float m21` | Valeur à la ligne 2 colonne 1 de la matrice. |
| `float m22` | Valeur à la ligne 2 colonne 2 de la matrice. |
| `float m23` | Valeur à la ligne 2, colonne 3 de la matrice. |
| `float m24` | Valeur à la ligne 2 colonne 4 de la matrice. |
| `float m31` | Valeur à la ligne 3 colonne 1 de la matrice. |
| `float m32` | Valeur à la ligne 3 colonne 2 de la matrice. |
| `float m33` | Valeur à la ligne 3 colonne 3 de la matrice. |
| `float m34` | Valeur à la ligne 3 colonne 4 de la matrice. |
| `float m41` | Valeur à la ligne 4 colonne 1 de la matrice. |
| `float m42` | Valeur à la ligne 4 colonne 2 de la matrice. |
| `float m43` | Valeur à la ligne 4 colonne 3 de la matrice. |
| `float m44` | Valeur à la ligne 4 colonne 4 de la matrice. |

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-|-|
| Espace de noms | Windows :: Foundation :: numerics |
| En-tête | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[API windowsnumerics. h](windowsnumerics-h-apis-portal.md)
