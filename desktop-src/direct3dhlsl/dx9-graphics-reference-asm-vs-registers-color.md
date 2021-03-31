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
ms.openlocfilehash: 38ee29ebafd9e7374fa868c6d84ad45f6c07dedf
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104321325"
---
# <a name="color-register"></a>Registre des couleurs

Ces registres de sortie du nuanceur de sommets contiennent une valeur de couleur. 

| S’inscrire | Description              |
|----------|--------------------------|
| oD0      | Registre des couleurs diffuses.  |
| oD1      | Registre de couleurs spéculaire. |



 

La valeur oD0 est interpolée et écrite dans le registre de couleurs du nuanceur de pixels 0 (v0). La valeur oD1 est interpolée et écrite dans le registre de couleurs du nuanceur de pixels 1 (v1). Pour plus d’informations sur les registres de couleurs du nuanceur de pixels, consultez la rubrique du [Registre des couleurs d’entrée](dx9-graphics-reference-asm-ps-registers-input-color.md) de nuanceur de pixels.

## <a name="remarks"></a>Notes

Exemple


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




