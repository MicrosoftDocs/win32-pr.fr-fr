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
ms.openlocfilehash: 4eb1af9bee9a571abf58fb20539945effc3ff1ee81cbb48a4d90c1510aebcd4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825279"
---
# <a name="float4-structure"></a>float4, structure

Vecteur avec quatre composants.

Ce type est disponible uniquement en C++. Son équivalent .NET est [System. Numerics. Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).

## <a name="constructors"></a>Constructeurs

| Nom | Description |
|-|-|
| `float4()` | Crée un float4 non initialisé. |
| `float4(float x, float y, float z, float w)` | Crée un float4 avec les valeurs spécifiées. |
| `float4(float2 value, float z, float w)` | Crée un float4 avec x et y copié à partir d’un float2 plus les valeurs z et w spécifiées. |
| `float4(float3 value, float w)` | Crée un float4 avec x, y et z copié à partir d’un float3 plus la valeur w spécifiée. |
| `explicit float4(float value)` | Crée un float4 avec l’ensemble de com. travau défini sur la valeur spécifiée. |
| `float4(Microsoft::?Graphics::?Canvas::?Numerics::?Vector4 const& value)` | Convertit un **Microsoft. Graphics. canevas. Numerics. Vector4** en float4. |

## <a name="functions"></a>Fonctions

| Nom | Description |
|-|-|
| `float length(float4 const& value)` | Calcule la longueur, ou distance euclidienne, du vecteur. |
| `float length_squared(float4 const& value)` | Calcule la longueur, ou distance euclidienne, du vecteur carré. |
| `float distance(float4 const& value1, float4 const& value2)` | Calcule la distance euclidienne entre deux vecteurs. |
| `float distance_squared(float4 const& value1, float4 const& value2)` | Calcule la distance euclidienne entre deux vecteurs carrés. |
| `float dot(float4 const& vector1, float4 const& vector2)` | Calcule le produit scalaire de deux vecteurs. |
| `float4 normalize(float4 const& vector)` | Crée un vecteur d’unité à partir du vecteur spécifié. |
| `float4 min(float4 const& value1, float4 const& value2)` | Retourne un vecteur qui contient la valeur la plus faible de chaque paire de composants correspondante. |
| `float4 max(float4 const& value1, float4 const& value2)` | Retourne un vecteur qui contient la valeur la plus élevée de chaque paire de composants correspondante. |
| `float4 clamp(float4 const& value1, float4 const& min, float4 const& max)` | Restreint une valeur à une plage spécifiée. |
| `float4 lerp(float4 const& value1, float4 const& value2, float amount)` | Effectue une interpolation linéaire entre deux vecteurs. |
| `float4 transform(float4 const& vector, float4x4 const& matrix)` | Transforme un float4 par la matrice donnée. |
| `float4 transform4(float3 const& position, float4x4 const& matrix)` | Transforme un float3 par la matrice donnée, en retournant un float4. |
| `float4 transform4(float2 const& position, float4x4 const& matrix)` | Transforme un float2 par la matrice donnée, en retournant un float4. |
| `float4 transform(float4 const& value, quaternion const& rotation)` | Transforme un float4 par le Quaternion donné. |
| `float4 transform4(float3 const& value, quaternion const& rotation)` | Transforme un float3 par le Quaternion donné, en retournant un float4. |
| `float4 transform4(float2 const& value, quaternion const& rotation)` | Transforme un float2 par le Quaternion donné, en retournant un float4. |

## <a name="methods"></a>Méthodes

| Nom | Description |
|-|-|
| `static float4 zero()` | Retourne un float4 avec tous ses composants définis sur zéro. |
| `static float4 one()` | Retourne un float4 avec tous ses composants définis sur un. |
| `static float4 unit_x()` | Retourne float4 (1, 0, 0, 0). |
| `static float4 unit_y()` | Retourne float4 (0, 1, 0, 0). |
| `static float4 unit_z()` | Retourne le float4 (0, 0, 1, 0). |
| `static float4 unit_w()` | Retourne le float4 (0, 0, 0, 1). |

## <a name="operators"></a>Opérateurs

| Nom | Description |
|-|-|
| `float4 operator+ (float4 const& value1, float4 const& value2)` | Ajoute deux vecteurs. |
| `float4 operator- (float4 const& value1, float4 const& value2)` | Soustrait un vecteur d’un vecteur. |
| `float4 operator* (float4 const& value1, float4 const& value2)` | Multiplie les composants de deux vecteurs. |
| `float4 operator* (float4 const& value1, float value2)` | Multiplie un vecteur par un scalaire. |
| `float4 operator* (float value1, float4 const& value2)` | Multiplie un vecteur par un scalaire. |
| `float4 operator/ (float4 const& value1, float4 const& value2)` | Divise les composants d’un vecteur par les composants d’un autre vecteur. |
| `float4 operator/ (float4 const& value1, float value2)` | Divise un vecteur par une valeur scalaire. |
| `float4 operator- (float4 const& value)` | Retourne un vecteur pointant dans la direction opposée. |
| `float4& operator+= (float4& value1, float4 const& value2)` | Sur place ajoute deux vecteurs. |
| `float4& operator-= (float4& value1, float4 const& value2)` | Sur place soustrait un vecteur d’un vecteur. |
| `float4& operator*= (float4& value1, float4 const& value2)` | Sur place, multiplie les composants de deux vecteurs. |
| `float4& operator*= (float4& value1, float value2)` | Sur place, multiplie un vecteur par un scalaire. |
| `float4& operator/= (float4& value1, float4 const& value2)` | Sur place, divise les composants d’un vecteur par les composants d’un autre vecteur. |
| `float4& operator/= (float4& value1, float value2)` | Sur place divise un vecteur par une valeur scalaire. |
| `bool operator== (float4 const& value1, float4 const& value2)` | Détermine si deux instances de float4 sont égales. |
| `bool operator!= (float4 const& value1, float4 const& value2)` | Détermine si deux instances de float4 ne sont pas égales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector4() const` | Convertit un float4 en un **Microsoft. Graphics. Canvas. Numerics. Vector4**. |

## <a name="fields"></a>Champs

| Nom | Description |
|-|-|
| `float x` | Composant X du vecteur. |
| `float y` | Composant Y du vecteur. |
| `float z` | Composant Z du vecteur. |
| `float w` | Composant W du vecteur. |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| Espace de noms | Windows :: Foundation :: numerics |
| En-tête | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[API windowsnumerics. h](windowsnumerics-h-apis-portal.md)
