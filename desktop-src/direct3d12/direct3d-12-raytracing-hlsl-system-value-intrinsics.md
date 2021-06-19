---
title: Intrinsèques de valeur système HLSL Direct3D 12 Raytracing
description: Affichez des liens vers des articles décrivant les fonctions intrinsèques de valeur système HLSL (High-Level Shader Language) qui prennent en charge le pipeline Raytracing Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2790cf5df42f64071db3ca51a35e58ee9afcd5
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396434"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a>Intrinsèques de valeur système HLSL Direct3D 12 Raytracing

Les valeurs système sont extraites à l’aide de fonctions intrinsèques spéciales, plutôt que d’inclure des paramètres avec une sémantique spéciale dans la signature de votre fonction de nuanceur. 

## <a name="in-this-section"></a>Contenu de cette section

### <a name="ray-dispatch-system-values"></a>Valeurs système de dispatch de rayon

| Rubrique | Description |
|-|-|
| [**DispatchRaysIndex**](dispatchraysindex.md) | Obtient l’emplacement x et y actuel dans la largeur et la hauteur obtenues avec la valeur système **DispatchRaysDimensions** intrinsèque. |
| [**DispatchRaysDimensions**](dispatchraysdimensions.md) | Valeurs de largeur, de hauteur et de profondeur de la structure **\_ \_ \_ desc des rayons D3D12 Dispatch** spécifiés dans l’appel **DispatchRays** d’origine. |

### <a name="ray-system-values"></a>Valeurs système de rayon

| Rubrique | Description |
|-|-|
| [**WorldRayOrigin**](worldrayorigin.md) | Origine de l’espace universel du rayon actuel. |
| [**WorldRayDirection**](worldraydirection.md) | Direction de l’espace universel pour le rayon actuel. |
| [**RayTMin**](raytmin.md) | Valeur float représentant le point de départ paramétrique actuel pour le rayon. |
| [**RayTCurrent**](raytcurrent.md) | Valeur float représentant le point de terminaison paramétrique actuel pour le rayon.  |
| [**RayFlags**](rayflags.md) | Entier non signé contenant les indicateurs de **ray_flag** actuels. |

### <a name="primitiveobject-space-system-values"></a>Valeurs système de l’espace de primitive/objet

| Rubrique | Description |
|-|-|
| [**InstanceIndex**](instanceindex.md) | Index généré automatiquement de l’instance actuelle dans la structure d’accélération de Raytracing de niveau supérieur. |
| [**InstanceID**](instanceid.md) | Identificateur fourni par l’utilisateur pour l’instance sur l’instance de la structure d’accélération de niveau inférieur dans la structure de niveau supérieur. |
| [**PrimitiveIndex**](primitiveindex.md) | Index généré automatiquement de la primitive dans la géométrie à l’intérieur de l’instance de la structure d’accélération de niveau inférieur. |
| [**ObjectRayOrigin**](objectrayorigin.md) | Origine de l’espace de l’objet pour le rayon actuel. |
| [**ObjectRayDirection**](objectraydirection.md) | Direction de l’espace de l’objet pour le rayon actuel. |
| [**ObjectToWorld3x4**](objecttoworld3x4.md) | Matrice pour la transformation de l’espace objet en espace universel. |
| [**ObjectToWorld4x3**](objecttoworld4x3.md) | Matrice pour la transformation de l’espace objet en espace universel. |
| [**WorldToObject3x4**](worldtoobject3x4.md) | Matrice pour la transformation de l’espace universel à l’espace d’objet |
| [**WorldToObject4x3**](worldtoobject4x3.md) | Matrice pour la transformation de l’espace universel à l’espace d’objet |
### <a name="hit-specific-system-values"></a>Valeurs système spécifiques à l’accès

| Rubrique | Description |
|-|-|
| [**HitKind**](hitkind.md) | Retourne la valeur passée comme paramètre **HitKind** à [**ReportHit**](reporthit-function.md). |

## <a name="related-topics"></a>Rubriques connexes

* [Référence principale](direct3d-12-core-reference.md)
* [Référence de Direct3D 12](direct3d-12-reference.md)
