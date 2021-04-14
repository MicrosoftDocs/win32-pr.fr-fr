---
description: Le mélangeur de mémoires tampons de frames peut désormais fusionner les canaux alpha indépendamment de la fusion des canaux de couleur sur les cibles de rendu. Ce contrôle est activé avec un nouvel état de rendu, D3DRS \_ SEPARATEALPHABLENDENABLE.
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: Rendu de la cible Alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70f395406559782172448b5555daff056ffd54c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520476"
---
# <a name="render-target-alpha-direct3d-9"></a>Rendu de la cible Alpha (Direct3D 9)

Le mélangeur de mémoires tampons de frames peut désormais fusionner les canaux alpha indépendamment de la fusion des canaux de couleur sur les cibles de rendu. Ce contrôle est activé avec un nouvel état de rendu, D3DRS \_ SEPARATEALPHABLENDENABLE.

Lorsque D3DRS \_ SEPARATEALPHABLENDENABLE est défini sur **false** (qui est la condition par défaut), les facteurs et les opérations de fusion de cible de rendu appliqués à alpha sont les mêmes que ceux définis pour la fusion des canaux de couleurs. Un pilote doit définir le \_ Cap SEPARATEALPHABLEND D3DPMISCCAPS pour indiquer qu’il peut prendre en charge la fusion alpha de rendu-cible. Veillez à activer D3DRS \_ ALPHABLEND pour indiquer au pipeline que la fusion alpha est nécessaire.

Pour contrôler les facteurs dans le canal alpha des mélangeurs de rendu-cible, deux nouveaux États de rendu sont définis comme suit :


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



À l’instar des D3DRS \_ SRCBLEND et D3DRS \_ DESTBLEND, ceux-ci peuvent être définis sur l’une des valeurs de l’énumération [**D3DBLEND**](./d3dblend.md) . Les paramètres de fusion de source et de destination peuvent être combinés de plusieurs façons, selon les paramètres des membres SrcBlendCaps et DestBlendCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

La fusion alpha s’effectue comme suit :

renderTargetAlpha = (alpha<sub>dans</sub> \* srcBlendOp) BlendOp (alpha<sub>RT</sub> \* destBlendOp)

Où :

-   Alpha<sub>dans</sub> est la valeur alpha d’entrée.
-   srcBlendOp est l’un des facteurs de mélange dans [**D3DBLEND**](./d3dblend.md).
-   BlendOp est l’un des facteurs de mélange dans [**D3DBLENDOP**](./d3dblendop.md).
-   Alpha<sub>RT</sub> est la valeur alpha Render-cible.
-   destBlendOp est l’un des facteurs de mélange dans [**D3DBLEND**](./d3dblend.md).
-   renderTargetAlpha est la valeur alpha fusionnée finale.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fusion alpha](alpha-blending.md)
</dt> </dl>

 

 
