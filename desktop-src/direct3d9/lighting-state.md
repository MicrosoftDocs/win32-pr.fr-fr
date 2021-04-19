---
description: Si vous ne vous contentez pas d’un nuanceur de sommets ou d’un nuanceur de pixels, vous pouvez choisir d’utiliser le moteur d’éclairage dans le Runtime.
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: État d’éclairage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74f0e7b7ec4a8bcf0ee27c9bc1e643536819d8fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515301"
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

 

 



