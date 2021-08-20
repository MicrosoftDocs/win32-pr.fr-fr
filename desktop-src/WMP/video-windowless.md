---
title: VIDÉO. sans fenêtre
description: L’attribut sans fenêtre spécifie ou récupère une valeur indiquant si le contrôle vidéo sera fenêtre ou sans fenêtre ; autrement dit, si le rectangle entier du contrôle est visible à tout moment ou s’il peut être coupé.
ms.assetid: d59e6baf-374b-48f6-b99f-35a83af7feb6
keywords:
- VIDEO. window Lecteur Windows Media
topic_type:
- apiref
api_name:
- VIDEO.windowless
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c98aefde5aab9837f220ccb7df254e6a592e0d5e9d41de43291b2ab73e287321
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117931739"
---
# <a name="videowindowless"></a>VIDÉO. sans fenêtre

L’attribut **sans fenêtre** spécifie ou récupère une valeur indiquant si le contrôle vidéo sera fenêtre ou sans fenêtre ; autrement dit, si le rectangle entier du contrôle est visible à tout moment ou s’il peut être coupé. Ne peut être défini qu’au moment de la conception.

``` syntax
        elementID.windowless
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** spécifiée au moment de la conception et en lecture seule par la suite.



| Valeur | Description                              |
|-------|------------------------------------------|
| true  | Le contrôle vidéo sera sans fenêtre.        |
| false | Par défaut. Le contrôle vidéo sera fenêtre. |



 

## <a name="remarks"></a>Remarques

Si vous souhaitez une fenêtre vidéo non rectangulaire ou si vous souhaitez couvrir une partie quelconque de la fenêtre vidéo avec une image, cet attribut doit avoir la valeur true. Cela sacrifie certaines performances pour effectuer l’écrêtage nécessaire.

La lecture vidéo est optimisée pour la lecture non découpée. Dans ce cas, l’attribut **sans fenêtre** est défini sur false et l’intégralité du rectangle vidéo est toujours affichée. Toute image couvrant la fenêtre vidéo est ignorée et la fenêtre vidéo a l’ordre de plan de niveau le plus élevé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément VIDEO**](video-element.md)
</dt> </dl>

 

 





