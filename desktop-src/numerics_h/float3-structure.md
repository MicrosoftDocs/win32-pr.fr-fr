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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525556"
---
# <a name="float3-structure"></a>float3, structure

Vecteur avec trois composants.

Ce type est disponible uniquement en C++. Son équivalent .NET est [System. Numerics. Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8).

## <a name="constructors"></a>Constructeurs

| Nom | Description |
|-|-|
| `float3()` | Crée un float3 non initialisé. |
| `float3(float x, float y, float z)` | Crée un float3 avec les valeurs spécifiées. |
| `float3(float2 value, float z)` | Crée un float3 avec x et y copié à partir d’un float2 plus la valeur z spécifiée. |
| `explicit float3(float value)` | Crée un float3 avec tous les composants définis sur la valeur spécifiée. |
| `float3(Microsoft::Graphics::Canvas::Numerics::Vector3 const& value)` | Convertit un **Microsoft. Graphics. canevas. Numerics. Vector3** en float3. |

## <a name="functions"></a>Fonctions

| Nom | Description |
|-|-|
| `float length(float3 const& value)` | Calcule la longueur, ou distance euclidienne, du vecteur. |
| `float length_squared(float3 const& value)` | Calcule la longueur, ou distance euclidienne, du vecteur carré. |
| `float distance(float3 const& value1, float3 const& value2)` | Calcule la distance euclidienne entre deux vecteurs. |
| `float distance_squared(float3 const& value1, float3 const& value2)` | Calcule la distance euclidienne entre deux vecteurs carrés. |
| `float dot(float3 const& vector1, float3 const& vector2)` | Calcule le produit scalaire de deux vecteurs. |
| `float3 normalize(float3 const& value)` | Crée un vecteur d’unité à partir du vecteur spécifié. |
| `float3 cross(float3 const& vector1, float3 const& vector2)` | Calcule le produit croisé de deux vecteurs. |
| `float3 reflect(float3 const& vector, float3 const& normal)` | Détermine le vecteur réfléchissant du vecteur donné et normal. |
| `float3 min(float3 const& value1, float3 const& value2)` | Retourne un vecteur qui contient la valeur la plus faible de chaque paire de composants correspondante. |
| `float3 max(float3 const& value1, float3 const& value2)` | Retourne un vecteur qui contient la valeur la plus élevée de chaque paire de composants correspondante. |
| `float3 clamp(float3 const& value1, float3 const& min, float3 const& max)` | Restreint une valeur à une plage spécifiée. |
| `float3 lerp(float3 const& value1, float3 const& value2, float amount)` | Effectue une interpolation linéaire entre deux vecteurs. |
| `float3 transform(float3 const& position, float4x4 const& matrix)` | Transforme le vecteur (x, y, z, 1) par la matrice spécifiée. |
| `float3 transform_normal(float3 const& normal, float4x4 const& matrix)` | Transforme le vecteur normal (x, y, z, 0) par la matrice spécifiée. |
| `float3 transform(float3 const& value, quaternion const& rotation)` | Transforme un float3 par le Quaternion donné. |

## <a name="methods"></a>Méthodes

| Nom | Description |
|-|-|
| `static float3 zero()` | Retourne un float3 avec tous ses composants définis sur zéro. |
| `static float3 one()` | Retourne un float3 avec tous ses composants définis sur un. |
| `static float3 unit_x()` | Retourne float3 (1, 0, 0). |
| `static float3 unit_y()` | Retourne float3 (0, 1, 0). |
| `static float3 unit_z()` | Retourne float3 (0, 0, 1). |

## <a name="operators"></a>Opérateurs

| Nom | Description |
|-|-|
| `float3 operator+ (float3 const& value1, float3 const& value2)` | Ajoute deux vecteurs. |
| `float3 operator- (float3 const& value1, float3 const& value2)` | Soustrait un vecteur d’un vecteur. |
| `float3 operator* (float3 const& value1, float3 const& value2)` | Multiplie les composants de deux vecteurs. |
| `float3 operator* (float3 const& value1, float value2)` | Multiplie un vecteur par un scalaire. |
| `float3 operator* (float value1, float3 const& value2)` | Multiplie un vecteur par un scalaire. |
| `float3 operator/ (float3 const& value1, float3 const& value2)` | Divise les composants d’un vecteur par les composants d’un autre vecteur. |
| `float3 operator/ (float3 const& value1, float value2)` | Divise un vecteur par une valeur scalaire. |
| `float3 operator- (float3 const& value)` | Retourne un vecteur pointant dans la direction opposée. |
| `float3& operator+= (float3& value1, float3 const& value2)` | Sur place ajoute deux vecteurs. |
| `float3& operator-= (float3& value1, float3 const& value2)` | Sur place soustrait un vecteur d’un vecteur. |
| `float3& operator*= (float3& value1, float3 const& value2)` | Sur place, multiplie les composants de deux vecteurs. |
| `float3& operator*= (float3& value1, float value2)` | Sur place, multiplie un vecteur par un scalaire. |
| `float3& operator/= (float3& value1, float3 const& value2)` | Sur place, divise les composants d’un vecteur par les composants d’un autre vecteur. |
| `float3& operator/= (float3& value1, float value2)` | Sur place divise un vecteur par une valeur scalaire. |
| `bool operator== (float3 const& value1, float3 const& value2)` | Détermine si deux instances de float3 sont égales. |
| `bool operator!= (float3 const& value1, float3 const& value2)` | Détermine si deux instances de float3 ne sont pas égales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector3() const` | Convertit un float3 en un **Microsoft. Graphics. Canvas. Numerics. Vector3**. |

## <a name="fields"></a>Champs

| Nom | Description |
|-|-|
| `float x` | Composant X du vecteur. |
| `float y` | Composant Y du vecteur. |
| `float z` | Composant Z du vecteur. |

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-|-|
| Espace de noms | Windows :: Foundation :: numerics |
| En-tête | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[API windowsnumerics. h](windowsnumerics-h-apis-portal.md)
