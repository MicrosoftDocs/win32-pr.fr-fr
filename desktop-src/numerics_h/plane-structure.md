---
title: structure du plan (Windowsnumerics. h)
description: Cette structure représente un plan à l’aide d’une valeur normale de vecteur 3D et d’une distance.
ms.assetid: 3C5A5EA0-8A51-4F9B-A84A-0C8E726CE3FD
keywords:
- structure du plan
topic_type:
- apiref
api_name:
- plane structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d870e2769121b4aec542235081011406e439d579
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526450"
---
# <a name="plane-structure"></a>structure du plan

Cette structure représente un plan à l’aide d’une valeur normale de vecteur 3D et d’une distance.

Ce type est disponible uniquement en C++. Son équivalent .NET est [System. Numerics. plan](/dotnet/api/system.numerics.plane?view=netframework-4.8).

## <a name="constructors"></a>Constructeurs

| Nom | Description |
|-|-|
| `plane()` | Crée un plan non initialisé. |
| `plane(float x, float y, float z, float d)` | Crée un plan avec les valeurs spécifiées. |
| `plane(float3 normal, float d)` | Crée un plan à partir d’un float3 et d’une distance. |
| `explicit plane(float4 value)` | Crée un plan à partir d’un float4. |
| `plane(Microsoft::?Graphics::?Canvas::?Numerics::?Plane const& value)` | Convertit un **Microsoft. Graphics. Canvas. Numerics. plan** en plan. |

## <a name="functions"></a>Fonctions

| Nom | Description |
|-|-|
| `plane make_plane_from_vertices(float3 const& point1, float3 const& point2, float3 const& point3)` | Crée un plan à partir d’un ensemble de trois positions de vertex, qui doivent toutes être différentes et ne pas être en ligne droite. |
| `plane normalize(plane const& value)` | Modifie les coefficients du vecteur normal d’un plan pour l’ajuster à la longueur de l’unité. |
| `plane transform(plane const& plane, float4x4 const& matrix)` | Transforme un plan normalisé par une matrice. |
| `plane transform(plane const& plane, quaternion const& rotation)` | Transforme un plan normalisé par une rotation de Quaternion. |
| `float dot(plane const& plane, float4 const& value)` | Calcule le produit scalaire d’un plan à l’aide d’un vecteur. |
| `float dot_coordinate(plane const& plane, float3 const& value)` | Calcule le produit scalaire d’un plan avec une coordonnée float3. Contrairement \_ au point normal, ce calcul comprend la valeur du plan d. |
| `float dot_normal(plane const& plane, float3 const& value)` | Calcule le produit scalaire d’un plan avec un float3 normal. Contrairement à \_ la coordonnée de points, ce calcul ignore la valeur du plan d. |

## <a name="operators"></a>Opérateurs

| Nom | Description |
|-|-|
| `bool operator== (plane const& value1, plane const& value2)` | Détermine si deux instances de plan sont égales. |
| `bool operator!= (plane const& value1, plane const& value2)` | Détermine si deux instances de plan ne sont pas égales. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Plane() const` | Convertit un plan en un **Microsoft. Graphics. canevas. Numerics. plan**. |

## <a name="fields"></a>Champs

| Nom | Description |
|-|-|
| `float3 normal` | Vecteur normal du plan. |
| `float d` | Distance du plan le long de sa normale par rapport à l’origine. |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| Espace de noms | Windows :: Foundation :: Numerics |
| En-tête | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[API windowsnumerics. h](windowsnumerics-h-apis-portal.md)
