---
title: Intrinsèques HLSL Direct3D 12 Raytracing
description: Affichez des liens vers des articles décrivant les fonctions intrinsèques HLSL (High-Level Shader Language) qui prennent en charge le pipeline Raytracing Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06687866354611f44f295ff4fe2cf171068e83c3
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396474"
---
# <a name="raytracing-hlsl-intrinsics"></a>Intrinsèques HLSL Raytracing

Les fonctions intrinisc HLSL suivantes prennent en charge le pipeline Direct3D 12 Raytracing. 

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique | Description |
|-|-|
| [**Fonction AcceptHitAndEndSearch**](accepthitandendsearch-function.md) | Utilisé dans un nuanceur de correspondance pour valider l’accès actuel, puis arrêter la recherche de plus d’accès pour le rayon. |
| [**Fonction CallShader**](callshader-function.md) | Appelle un autre nuanceur à partir d’un nuanceur. |
| [**Fonction IgnoreHit**](ignorehit-function.md) | Appelée à partir d’un nuanceur d’accès quelconque pour rejeter l’accès et terminer le nuanceur. |
| [**PrimitiveIndex fonction)**](primitiveindex.md) | Récupère l’index généré automatiquement de la primitive dans la géométrie à l’intérieur de l’instance de la structure d’accélération de niveau inférieur. |
| [**Fonction ReportHit**](reporthit-function.md) | Appelé par un nuanceur d’intersection pour signaler une intersection de rayon. |
| [**Fonction TraceRay**](traceray-function.md) | Envoie un rayon dans une recherche de correspondances dans une structure d’accélération. |

## <a name="related-topics"></a>Rubriques connexes

* [Référence principale](direct3d-12-core-reference.md)
* [Référence de Direct3D 12](direct3d-12-reference.md)
