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
# <a name="quaternion-structure"></a>Quaternion, structure

Vecteur à quatre dimensions, utilisé pour représenter une rotation.

Un Quaternion peut faire pivoter efficacement un objet autour du vecteur (x, y, z) par le thêta angulaire, où w = cos (thêta/2). Les quaternions sont généralement utilisés pour l’interpolation lisse entre deux angles, et pour éviter le problème de verrou à cardan qui peut se produire avec des angles Euler.

Ce type est disponible uniquement en C++. Son équivalent .NET est [System. Numerics. Quaternion](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).

## <a name="constructors"></a>Constructeurs

| Nom | Description |
|-|-|
| `quaternion()` | Crée un Quaternion non initialisé. |
| `quaternion(float x, float y, float z, float w)` | Crée un Quaternion avec les valeurs spécifiées. |
| `quaternion(float3 vectorPart, float scalarPart)` | Crée un Quaternion à partir d’un float3 et d’un scalaire. |
| `quaternion(Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion const& value)` | Convertit un **Microsoft. Graphics. canevas. Numerics. Quaternion** en un Quaternion. |

## <a name="functions"></a>Fonctions

| Nom | Description |
|-|-|
| `quaternion make_quaternion_from_axis_angle(float3 const& axis, float angle)` | Crée un quaternion à partir d'un vecteur et d'un angle de rotation sur le vecteur. |
| `quaternion make_quaternion_from_yaw_pitch_roll(float yaw, float pitch, float roll)` | Crée un Quaternion à partir de l’angle de lacet, du tangage et du roulis spécifiés. |
| `quaternion make_quaternion_from_rotation_matrix(float4x4 const& matrix)` | Crée un Quaternion à partir d’une matrice de rotation. |
| `bool is_identity(quaternion const& value)` | Vérifie s’il s’agit d’une identité (pas de rotation) Quaternion. |
| `float length(quaternion const& value)` | Calcule la longueur d’un Quaternion. |
| `float length_squared(quaternion const& value)` | Calcule la longueur au carré d’un Quaternion. |
| `float dot(quaternion const& quaternion1, quaternion const& quaternion2)` | Calcule le produit scalaire de deux quaternions. |
| `quaternion normalize(quaternion const& value)` | Divise chaque composant d’un Quaternion par la longueur du Quaternion. |
| `quaternion conjugate(quaternion const& value)` | Calcule le conjugué d’un Quaternion. |
| `quaternion inverse(quaternion const& value)` | Calcule l’inverse d’un Quaternion. |
| `quaternion slerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | Effectue une interpolation entre deux quaternions, en utilisant une interpolation linéaire sphérique. |
| `quaternion lerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | Interpole de manière linéaire entre deux quaternions. |
| `quaternion concatenate(quaternion const& value1, quaternion const& value2)` | Concatène deux quaternions ; le résultat représente la première rotation suivie de la deuxième rotation. |

## <a name="methods"></a>Méthodes

| Nom | Description |
|-|-|
| `static quaternion identity()` | Retourne une instance du Quaternion d’identité. |

## <a name="operators"></a>Opérateurs

| Nom | Description |
|-|-|
| `quaternion operator+ (quaternion const& value1, quaternion const& value2)` | Ajoute deux quaternions. |
| `quaternion operator- (quaternion const& value1, quaternion const& value2)` | Soustrait un Quaternion d’un autre Quaternion. |
| `quaternion operator* (quaternion const& value1, quaternion const& value2)` | Multiplie un Quaternion par un autre Quaternion. |
| `quaternion operator* (quaternion const& value1, float value2)` | Multiplie un Quaternion par une valeur scalaire. |
| `quaternion operator/ (quaternion const& value1, quaternion const& value2)` | Divise un Quaternion par un autre Quaternion. |
| `quaternion operator- (quaternion const& value)` | Retourne le signe de chaque composant du Quaternion. |
| `quaternion& operator+= (quaternion& value1, quaternion const& value2)` | Sur place ajoute deux quaternions. |
| `quaternion& operator-= (quaternion& value1, quaternion const& value2)` | Sur place soustrait un Quaternion d’un autre Quaternion. |
| `quaternion& operator*= (quaternion& value1, quaternion const& value2)` | Sur place, multiplie un Quaternion par un autre Quaternion. |
| `quaternion& operator*= (quaternion& value1, float value2)` | Nultiplies sur place un Quaternion par une valeur scalaire. |
| `quaternion& operator/= (quaternion& value1, quaternion const& value2)` | Sur place, divise un Quaternion par un autre Quaternion. |
| `bool operator== (quaternion const& value1, quaternion const& value2)` | Détermine si deux instances de Quaternion sont égales. |
| `bool operator!= (quaternion const& value1, quaternion const& value2)` | Détermine si deux instances de Quaternion ne sont pas égales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion() const` | Convertit un quaternion en un **Microsoft. Graphics. canevas. Numerics. Quaternion**. |

## <a name="fields"></a>Champs

| Nom | Description |
|-|-|
| `float x` | Valeur X du composant vecteur du Quaternion. |
| `float y` | Valeur Y du composant vecteur du Quaternion. |
| `float z` | Valeur Z du composant vecteur du Quaternion. |
| `float w` | Composant de rotation du Quaternion. |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| Espace de noms | Windows :: Foundation :: Numerics |
| En-tête | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[API windowsnumerics. h](windowsnumerics-h-apis-portal.md)
