---
description: Le moteur d’éclairage Direct3D peut utiliser les données de couleur par vertex lors de l’éclairage si vous indiquez au runtime que les données sont présentes.
ms.assetid: acb43921-f0d4-4151-9371-1b99e5d30c0e
title: État de la couleur de l' Per-Vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6efd227c64785f7399ae3ba56d4623342c0910d901c3cfc404fc4a37f0d233
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727983"
---
# <a name="per-vertex-color-state-direct3d-9"></a>État de la couleur de l' Per-Vertex (Direct3D 9)

Le moteur d’éclairage Direct3D peut utiliser les données de couleur par vertex lors de l’éclairage si vous indiquez au runtime que les données sont présentes. Pour ce faire, activez l’état de rendu suivant :


```
// disable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, FALSE);

// enable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, TRUE);
```



Si la couleur par vertex est activée, les applications peuvent configurer la source à partir de laquelle le système récupère les informations de couleur pour un vertex. Les \_ États de rendu D3DRS AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE et D3DRS SPECULARMATERIALSOURCE \_ contrôlent respectivement les sources de composant de couleur ambiante, diffuse, émissif et spéculaire. Chaque État peut être défini sur des membres du type énuméré [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) , qui définit des constantes qui indiquent au système d’utiliser la matière actuelle, la couleur diffuse ou la couleur spéculaire comme source pour le composant de couleur spécifié.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[États de rendu](render-states.md)
</dt> </dl>

 

 
