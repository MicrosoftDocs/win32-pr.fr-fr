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
ms.openlocfilehash: ee3bffcfd86ba48d737066bd2ca56e6b124a59412704c5f30952e5a70ae71e24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952039"
---
# <a name="float2-structure"></a>float2, structure

Vecteur avec deux composants.

Ce type est disponible uniquement en C++. Son équivalent .NET est [System. Numerics. Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).

## <a name="constructors"></a>Constructeurs

| Nom | Description |
|-|-|
| `float2()` | Crée un float2 non initialisé. |
| `float2(float x, float y)` | Crée un float2 avec les valeurs spécifiées. |
| `explicit float2(float value)` | Crée un float2 avec tous les composants définis sur la valeur spécifiée. |
| `float2(Microsoft::Graphics::Canvas::Numerics::Vector2 const& value)` | Convertit un **Microsoft. Graphics. canevas. Numerics. Vector2** en float2. |
| `float2(Windows::Foundation::Point const& value)` | Convertit une [**Windows. Fondation. pointez**](/uwp/api/Windows.Foundation.Point) sur un float2. |
| `float2(Windows::Foundation::Size const& value)` | Convertit une [**Windows. Foundation. Size**](/uwp/api/Windows.Foundation.Size) à un float2. |

## <a name="functions"></a>Fonctions

| Nom | Description |
|-|-|
| `float length(float2 const& value)` | Calcule la longueur, ou distance euclidienne, du vecteur. |
| `float length_squared(float2 const& value)` | Calcule la longueur, ou distance euclidienne, du vecteur carré. |
| `float distance(float2 const& value1, float2 const& value2)` | Calcule la distance euclidienne entre deux vecteurs. |
| `float distance_squared(float2 const& value1, float2 const& value2)` | Calcule la distance euclidienne entre deux vecteurs carrés. |
| `float dot(float2 const& value1, float2 const& value2)` | Calcule le produit scalaire de deux vecteurs. |
| `float2 normalize(float2 const& value)` | Crée un vecteur d’unité à partir du vecteur spécifié. |
| `float2 reflect(float2 const& vector, float2 const& normal)` | Détermine le vecteur réfléchissant du vecteur donné et normal. |
| `float2 min(float2 const& value1, float2 const& value2)` | Retourne un vecteur qui contient la valeur la plus faible de chaque paire de composants correspondante. |
| `float2 max(float2 const& value1, float2 const& value2)` | Retourne un vecteur qui contient la valeur la plus élevée de chaque paire de composants correspondante. |
| `float2 clamp(float2 const& value1, float2 const& min, float2 const& max)` | Restreint une valeur à une plage spécifiée. |
| `float2 lerp(float2 const& value1, float2 const& value2, float amount)` | Effectue une interpolation linéaire entre deux vecteurs. |
| `float2 transform(float2 const& position, float3x2 const& matrix)` | Transforme le vecteur (x, y, 0, 1) par la matrice spécifiée. |
| `float2 transform(float2 const& position, float4x4 const& matrix)` | Transforme le vecteur (x, y, 0, 1) par la matrice spécifiée. |
| `float2 transform_normal(float2 const& normal, float3x2 const& matrix)` | Transforme le vecteur normal (x, y, 0, 0) par la matrice spécifiée. |
| `float2 transform_normal(float2 const& normal, float4x4 const& matrix)` | Transforme le vecteur normal (x, y, 0, 0) par la matrice spécifiée. |
| `float2 transform(float2 const& value, quaternion const& rotation)` | Transforme un float2 par le Quaternion donné. |

## <a name="methods"></a>Méthodes

| Nom | Description |
|-|-|
| `static float2 zero()` | Retourne un float2 avec tous ses composants définis sur zéro. |
| `static float2 one()` | Retourne un float2 avec tous ses composants définis sur un. |
| `static float2 unit_x()` | Retourne le float2 (1,0). |
| `static float2 unit_y()` | Retourne le float2 (0, 1). |

## <a name="operators"></a>Opérateurs

| Nom | Description |
|-|-|
| `operator Windows::Foundation::Point() const` | Convertit un float2 en [**Windows. Fondation. point**](/uwp/api/Windows.Foundation.Point). |
| `operator Windows::Foundation::Size() const` | Convertit un float2 en [**Windows. Foundation. Size**](/uwp/api/Windows.Foundation.Size). |
| `float2 operator+ (float2 const& value1, float2 const& value2)` | Ajoute deux vecteurs. |
| `float2 operator- (float2 const& value1, float2 const& value2)` | Soustrait un vecteur d’un vecteur. |
| `float2 operator* (float2 const& value1, float2 const& value2)` | Multiplie les composants de deux vecteurs. |
| `float2 operator* (float2 const& value1, float value2)` | Multiplie un vecteur par un scalaire. |
| `float2 operator* (float value1, float2 const& value2)` | Multiplie un vecteur par un scalaire. |
| `float2 operator/ (float2 const& value1, float2 const& value2)` | Divise les composants d’un vecteur par les composants d’un autre vecteur. |
| `float2 operator/ (float2 const& value1, float value2)` | Divise un vecteur par une valeur scalaire. |
| `float2 operator- (float2 const& value)` | Retourne un vecteur pointant dans la direction opposée. |
| `float2& operator+= (float2& value1, float2 const& value2)` | Sur place ajoute deux vecteurs. |
| `float2& operator-= (float2& value1, float2 const& value2)` | Sur place soustrait un vecteur d’un vecteur. |
| `float2& operator*= (float2& value1, float2 const& value2)` | Sur place, multiplie les composants de deux vecteurs. |
| `float2& operator*= (float2& value1, float value2)` | Sur place, multiplie un vecteur par un scalaire. |
| `float2& operator/= (float2& value1, float2 const& value2)` | Sur place, divise les composants d’un vecteur par les composants d’un autre vecteur. |
| `float2& operator/= (float2& value1, float value2)` | Sur place divise un vecteur par une valeur scalaire. |
| `bool operator== (float2 const& value1, float2 const& value2)` | Détermine si deux instances de float2 sont égales. |
| `bool operator!= (float2 const& value1, float2 const& value2)` | Détermine si deux instances de float2 ne sont pas égales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector2() const` | Convertit un float2 en un **Microsoft. Graphics. Canvas. Numerics. Vector2**. |

## <a name="fields"></a>Champs

| Nom | Description |
|-|-|
| `float x` | Composant X du vecteur. |
| `float y` | Composant Y du vecteur. |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| Espace de noms | Windows :: Foundation :: numerics |
| En-tête | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[API windowsnumerics. h](windowsnumerics-h-apis-portal.md)
