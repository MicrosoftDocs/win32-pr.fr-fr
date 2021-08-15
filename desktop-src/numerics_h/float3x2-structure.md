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
ms.openlocfilehash: 24d403446fa3544bdb001c065e9874f812a829680e19a5e6b526ed12276fd6e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971758"
---
# <a name="float3x2-structure"></a>float3x2, structure

Matrice matrice, utilisée pour les transformations 2D.

Ce type de matrice utilise une disposition de vecteur de ligne. Les coordonnées x et y du vecteur de translation de cette matrice correspondent aux champs M31, M32.

Ce type est disponible uniquement en C++. Son équivalent .NET est [System. Numerics. Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).

## <a name="constructors"></a>Constructeurs

| Nom | Description |
|-|-|
| `float3x2()` | Crée un float3x2 non initialisé. |
| `float3x2(float m11, float m12, float m21, float m22, float m31, float m32)` | Crée un float3x2 avec les valeurs spécifiées. |
| `float3x2(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2 const& value)` | Convertit un **Microsoft. Graphics. canevas. Numerics. Matrix3x2** en float3x2. |

## <a name="functions"></a>Fonctions

| Nom | Description |
|-|-|
| `float3x2 make_float3x2_translation(float2 const& position)` | Crée une matrice de translation. |
| `float3x2 make_float3x2_translation(float xPosition, float yPosition)` | Crée une matrice de translation. |
| `float3x2 make_float3x2_scale(float xScale, float yScale)` | Crée une matrice de mise à l’échelle, centrée sur l’origine. |
| `float3x2 make_float3x2_scale(float xScale, float yScale, float2 const& centerPoint)` | Crée une matrice de mise à l’échelle, centrée sur le point spécifié. |
| `float3x2 make_float3x2_scale(float2 const& scales)` | Crée une matrice de mise à l’échelle, centrée sur l’origine. |
| `float3x2 make_float3x2_scale(float2 const& scales, float2 const& centerPoint)` | Crée une matrice de mise à l’échelle, centrée sur le point spécifié. |
| `float3x2 make_float3x2_scale(float scale)` | Crée une matrice de mise à l’échelle, centrée sur l’origine. |
| `float3x2 make_float3x2_scale(float scale, float2 const& centerPoint)` | Crée une matrice de mise à l’échelle, centrée sur le point spécifié. |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY)` | Crée une matrice inclinée, centrée sur l’origine. |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY, float2 const& centerPoint)` | Crée une matrice d’inclinaison, centrée sur le point spécifié. |
| `float3x2 make_float3x2_rotation(float radians)` | Crée une matrice de rotation, centrée sur l’origine. |
| `float3x2 make_float3x2_rotation(float radians, float2 const& centerPoint)` | Crée une matrice de rotation, centrée sur le point spécifié. |
| `bool is_identity(float3x2 const& value)` | Vérifie s’il s’agit d’une matrice d’identité. |
| `float determinant(float3x2 const& value)` | Calcule le déterminant de la matrice. |
| `float2 translation(float3x2 const& value)` | Obtient le vecteur de translation de la matrice. |
| `bool invert(float3x2 const& matrix, _Out_ float3x2* result)` | Calcule l’inverse d’une matrice. Retourne la valeur true si la matrice peut être inversée ; false dans le cas contraire. |
| `float3x2 lerp(float3x2 const& matrix1, float3x2 const& matrix2, float amount)` | Interpole de manière linéaire entre les valeurs correspondantes de deux matrices. |

## <a name="methods"></a>Méthodes

| Nom | Description |
|-|-|
| `static float3x2 identity()` | Retourne une instance de la matrice d’identité. |

## <a name="operators"></a>Opérateurs

| Nom | Description |
|-|-|
| `float3x2 operator+ (float3x2 const& value1, float3x2 const& value2)` | Ajoute chaque composant d’une matrice à une autre matrice. |
| `float3x2 operator- (float3x2 const& value1, float3x2 const& value2)` | Soustrait chaque composant d’une matrice d’une autre matrice. |
| `float3x2 operator* (float3x2 const& value1, float3x2 const& value2)` | Multiplie une matrice par une autre matrice. Cela a pour effet de concaténer deux transformations. |
| `float3x2 operator* (float3x2 const& value1, float value2)` | Multiplie chaque composant d’une matrice par une valeur scalaire. |
| `float3x2 operator- (float3x2 const& value)` | Nie chaque composant d’une matrice. |
| `float3x2& operator+= (float3x2& value1, float3x2 const& value2)` | Sur place ajoute chaque composant d’une matrice à une autre matrice. |
| `float3x2& operator-= (float3x2& value1, float3x2 const& value2)` | Sur place soustrait chaque composant d’une matrice d’une autre matrice. |
| `float3x2& operator*= (float3x2& value1, float3x2 const& value2)` | Sur place, une matrice est multipliée par une autre matrice. Cela a pour effet de concaténer deux transformations. |
| `float3x2& operator*= (float3x2& value1, float value2)` | Sur place multiplie chaque composant d’une matrice par une valeur scalaire. |
| `bool operator== (float3x2 const& value1, float3x2 const& value2)` | Détermine si deux instances de float3x2 sont égales. |
| `bool operator!= (float3x2 const& value1, float3x2 const& value2)` | Détermine si deux instances de float3x2 ne sont pas égales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2() const` | Convertit un float3x2 en un **Microsoft. Graphics. Canvas. Numerics. Matrix3x2**. |

## <a name="fields"></a>Champs

| Nom | Description |
|-|-|
| `float m11` | Valeur à la ligne 1 colonne 1 de la matrice. |
| `float m12` | Valeur à la ligne 1, colonne 2 de la matrice. |
| `float m21` | Valeur à la ligne 2 colonne 1 de la matrice. |
| `float m22` | Valeur à la ligne 2 colonne 2 de la matrice. |
| `float m31` | Valeur à la ligne 3 colonne 1 de la matrice. |
| `float m32` | Valeur à la ligne 3 colonne 2 de la matrice. |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| Espace de noms | Windows :: Foundation :: numerics |
| En-tête | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[API windowsnumerics. h](windowsnumerics-h-apis-portal.md)
