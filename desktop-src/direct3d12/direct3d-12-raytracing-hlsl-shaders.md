---
title: Nuanceurs HLSL Direct3D 12 Raytracing
description: Affichez des liens vers des articles décrivant les nuanceurs HLSL (High-Level Shader Language) qui prennent en charge le pipeline Raytracing Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca19081b1ea963851e82d18912153434c3e38d1
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394834"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a>Nuanceurs HLSL Direct3D 12 Raytracing

Les nuanceurs HLSL suivants prennent en charge le pipeline Direct3D 12 Raytracing. Ces nuanceurs sont des fonctions compilées dans une bibliothèque, avec lib_6_3 de modèle cible et identifiées par un attribut *[Shader ("shadertype")]* sur la fonction de nuanceur. Consultez valeurs **intrinsèques** et **valeurs système** pour voir ce qui est autorisé pour chaque type de nuanceur.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                       | Description                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Tout nuanceur de correspondance**](any-hit-shader.md)<br/>                              | Un nuanceur qui est appelé quand les intersections de rayon ne sont pas opaques.<br/>                                                                                                                                                                                                                                              |
| [**Nuanceur pouvant être appelé**](callable-shader.md)<br/>                              | Un nuanceur qui est appelé à partir d’un autre nuanceur avec l’intrinsèque **CallShader** .<br/>                                                                                                                                                                                                                                              |
| [**Nuanceur de correspondance le plus proche**](closest-hit-shader.md)<br/>                              | Nuanceur appelé lorsqu’il est activé et que l’accès le plus proche a été déterminé ou que la recherche d’intersection de rayon s’est terminée.<br/>                                                                                                                                                                                                                                              |
| [**Nuanceur d’intersection**](intersection-shader.md)<br/>                              | Nuanceur utilisé pour implémenter des primitives d’intersection personnalisées pour les rayons qui croisent un volume englobant associé (cadre englobant).<br/>                                                                                                                                                                                                                                              |
| [**Nuanceur manque**](miss-shader.md)<br/>                              | Nuanceur qui est appelé quand aucune intersection de rayon n’est trouvée ou acceptée.<br/>                                                                                                                                                                                                                                              |
| [**Nuanceur de création de rayon**](ray-generation-shader.md)<br/>                              | Nuanceur qui appelle [**TraceRay**](traceray-function.md) pour générer des rayons.<br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence principale](direct3d-12-core-reference.md)
</dt> <dt>

[Référence de Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 





