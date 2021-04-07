---
description: Les paramètres de brouillard sont contrôlés par le biais d’États de rendu d’appareil.
ms.assetid: a3c5f439-6937-4ba9-991f-5a4154447cf9
title: Paramètres de brouillard (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03104df36aba0868c15ccc0b8ddc78d1352bef7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846173"
---
# <a name="fog-parameters-direct3d-9"></a>Paramètres de brouillard (Direct3D 9)

Les paramètres de brouillard sont contrôlés par le biais d’États de rendu d’appareil. Les types de brouillard de pixel et de vertex prennent en charge toutes les formules de brouillard introduites dans des [formules de brouillard (Direct3D 9)](fog-formulas.md). Le type énuméré [**D3DFOGMODE**](./d3dfogmode.md) définit des constantes que vous pouvez utiliser pour identifier la formule de brouillard que vous souhaitez que Microsoft Direct3D utilise. L' \_ État de rendu D3DRS FOGTABLEMODE contrôle le mode de brouillard utilisé par Direct3D pour le brouillard de pixel, tandis que l' \_ État de rendu D3DRS FOGVERTEXMODE contrôle le mode du brouillard de vertex.

Lorsque vous utilisez la formule de brouillard linéaire, vous définissez les distances de début et de fin via les \_ États de rendu D3DRS FOGSTART et D3DRS \_ FOGEND. La façon dont le système interprète ces valeurs dépend du type de brouillard utilisé par votre application : pixel ou brouillard de vertex, et, lors de l’utilisation du brouillard de pixel, si une profondeur z ou w est utilisée. Le tableau suivant résume les types de brouillard et leurs unités de début et de fin.



| Type de brouillard  | Unités de début/fin du brouillard      |
|-----------|--------------------------|
| Pixel (Z) | Espace \[ de périphérique 0.0, 1.0\] |
| Pixel (W) | Espace de l’appareil photo             |
| Sommet    | Espace de l’appareil photo             |



 

L' \_ État de rendu D3DRS FOGDENSITY contrôle la densité de brouillard appliquée quand une formule de brouillard exponentiel est activée. La densité de brouillard est essentiellement un facteur de pondération, allant de 0,0 à 1,0 (inclus), qui met à l’échelle la valeur de distance dans l’exposant.

La couleur utilisée par le système pour la fusion de brouillard est contrôlée par le biais de l’état de rendu de l' \_ appareil D3DRS FOGCOLOR. Pour plus d’informations, consultez [couleur de brouillard (Direct3D 9)](fog-color.md) et [mélange de brouillards (Direct3D 9)](fog-blending.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de brouillard](fog-types.md)
</dt> </dl>

 

 
