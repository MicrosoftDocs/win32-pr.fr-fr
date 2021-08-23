---
description: Pour améliorer les performances de rendu, vous pouvez supprimer (ou supprimer) une primitive qui s’éloigne de l’appareil photo.
ms.assetid: b4b8ff3f-aa20-4422-8f6f-34cae25de0e6
title: État d’élimination (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bf9d8ed8ecea46dcfee146784dc97a38e42f0261b8f78bfc9d45ffaf99ddd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608029"
---
# <a name="culling-state-direct3d-9"></a>État d’élimination (Direct3D 9)

Pour améliorer les performances de rendu, vous pouvez supprimer (ou supprimer) une primitive qui s’éloigne de l’appareil photo. Pour les primitives à un seul côté, Cela économise l’heure de rendu, car une face arrière n’est pas visible. Pour activer l’élimination, vous devez connaître l’ordre d’enroulement des vertex (généralement dans le sens inverse des aiguilles d’une montre). Cet exemple supprime toutes les primitives dont la face arrière est dirigée vers l’avant (selon un sens dans le sens inverse des aiguilles d’une montre) :


```
SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[États de rendu](render-states.md)
</dt> </dl>

 

 



