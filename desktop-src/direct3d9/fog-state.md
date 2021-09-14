---
description: Les effets de brouillard peuvent offrir une scène 3D plus réaliste.
ms.assetid: 26fe4f7c-7bb3-4a52-b539-5de2b11256e9
title: État de brouillard (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d3103cbbd3dfb220e2ddd75078040702fd7557
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916580"
---
# <a name="fog-state-direct3d-9"></a>État de brouillard (Direct3D 9)

Les effets de brouillard peuvent offrir une scène 3D plus réaliste. Vous pouvez utiliser des effets de brouillard pour plus de simulation du brouillard. Ils peuvent également réduire la clarté d’une scène avec une distance. Cela reflète ce qui se passe dans le monde réel. comme les objets deviennent plus éloignés de l’utilisateur, leurs détails sont moins distincts.

Pour plus d’informations sur l’utilisation du brouillard dans votre application, consultez [brouillard (Direct3D 9)](fog.md).

Une application C++ contrôle le brouillard via les États de rendu de l’appareil. Le type énuméré [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) comprend des États pour contrôler si le brouillard de pixel (table) ou de vertex est utilisé, la couleur qu’il est, la formule de brouillard appliquée par le système et les paramètres de la formule.

Vous activez le brouillard en affectant \_ à l’état de rendu D3DRS FOGENABLE la **valeur true**. La couleur de brouillard peut être définie sur n’importe quelle valeur de couleur à l’aide de l' \_ État de rendu D3DRS FOGCOLOR ; le composant alpha de la couleur de brouillard est ignoré.

Les \_ États de rendu D3DRS FOGTABLEMODE et D3DRS \_ FOGVERTEXMODE contrôlent la formule de brouillard appliquée pour les calculs de brouillard et ils contrôlent indirectement le type de brouillard appliqué. Les deux États de rendu peuvent être définis sur un membre du type énuméré [**D3DFOGMODE**](./d3dfogmode.md) . La définition de l’état de rendu sur D3DFOG \_ None désactive le brouillard de pixel ou vertex, respectivement. Si les deux États de rendu sont définis sur des modes valides, le système applique uniquement les effets de brouillard de pixel.

Les \_ États de rendu D3DRS FOGSTART et D3DRS \_ FOGEND contrôlent les paramètres de formule de brouillard pour le \_ mode D3DFOG Linear. L' \_ État de rendu D3DRS FOGDENSITY contrôle la densité de brouillard dans les modes de brouillard exponentiels.

Pour plus d’informations, consultez [paramètres de brouillard (Direct3D 9)](fog-parameters.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[États de rendu](render-states.md)
</dt> </dl>

 

 
