---
description: L’interpolation de vertex fusionne deux positions fournies par l’utilisateur (ou normales).
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: Interpolation de vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8486f53e4eb1a3a003b15255baeb50d30f0ed205f4259625d7d66ba33e8274c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519220"
---
# <a name="vertex-tweening-direct3d-9"></a>Interpolation de vertex (Direct3D 9)

L’interpolation de vertex fusionne deux positions fournies par l’utilisateur (ou normales). L’interpolation s’exclut mutuellement de la fusion de vertex avec des poids. L’interpolation est effectuée avant l’éclairage et le découpage, et est activée en définissant D3DRS \_ VERTEXBLEND sur l' \_ interpolation D3DVBF. La position du vertex résultante est calculée par :


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



La même approche est utilisée pour le calcul des normales. Pour plus d’informations, consultez [utilisation de l’interpolation de vertex (Direct3D 9)](using-vertex-tweening.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fusion géométrique](geometry-blending.md)
</dt> </dl>

 

 



