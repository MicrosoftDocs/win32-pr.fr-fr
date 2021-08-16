---
title: Registre des couleurs
description: Ces registres de sortie du nuanceur de sommets contiennent une valeur de couleur.
ms.assetid: fd36e207-7312-4c7e-b664-b2de9ba1ebcf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b19850985002ad9c36a6a6366f744106cb041db858f9df9b755996e114fdf6c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512285"
---
# <a name="color-register"></a>Registre des couleurs

Ces registres de sortie du nuanceur de sommets contiennent une valeur de couleur. 

| S’inscrire | Description              |
|----------|--------------------------|
| oD0      | Registre des couleurs diffuses.  |
| oD1      | Registre de couleurs spéculaire. |



 

La valeur oD0 est interpolée et écrite dans le registre de couleurs du nuanceur de pixels 0 (v0). La valeur oD1 est interpolée et écrite dans le registre de couleurs du nuanceur de pixels 1 (v1). Pour plus d’informations sur les registres de couleurs du nuanceur de pixels, consultez la rubrique du [Registre des couleurs d’entrée](dx9-graphics-reference-asm-ps-registers-input-color.md) de nuanceur de pixels.

## <a name="remarks"></a>Remarques

 Exemple


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




