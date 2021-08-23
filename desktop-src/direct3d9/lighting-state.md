---
description: Si vous ne vous contentez pas d’un nuanceur de sommets ou d’un nuanceur de pixels, vous pouvez choisir d’utiliser le moteur d’éclairage dans le Runtime.
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: État d’éclairage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5935590c46776c621535968f4d457f3738d83d02342ffddf832cbf0278bbd9ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674269"
---
# <a name="lighting-state-direct3d-9"></a>État d’éclairage (Direct3D 9)

Si vous ne vous contentez pas d’un nuanceur de sommets ou d’un nuanceur de pixels, vous pouvez choisir d’utiliser le moteur d’éclairage dans le Runtime. Le moteur d’éclairage exige que les données de vertex contiennent des normales par vertex ; les vertex sans données normales génèrent un produit scalaire de zéro dans tous les calculs d’éclairage. Les calculs d’éclairage sont traités plus en détail dans l' [éclairage mathématique (Direct3D 9)](mathematics-of-lighting.md).

Pour activer le moteur d’éclairage, utilisez :


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[États de rendu](render-states.md)
</dt> </dl>

 

 



