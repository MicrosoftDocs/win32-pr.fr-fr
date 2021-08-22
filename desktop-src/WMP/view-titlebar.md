---
title: VIEW. titleBar
description: L’attribut titleBar récupère une valeur indiquant si la barre de titre de la fenêtre est affichée.
ms.assetid: 996aa2e0-0313-4a48-adcb-b82f76f38b6a
keywords:
- VIEW. titleBar Lecteur Windows Media
topic_type:
- apiref
api_name:
- VIEW.titleBar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb05550c22c342d14690f24f42c62a3af328eae65201b8138e82a7a33bf99fb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054067"
---
# <a name="viewtitlebar"></a>VIEW. titleBar

L’attribut **TitleBar** récupère une valeur indiquant si la barre de titre de la fenêtre est affichée.

``` syntax
        elementID.titleBar
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture seule.



| Valeur | Description                             |
|-------|-----------------------------------------|
| true  | Par défaut. La barre de titre de la fenêtre s’affiche. |
| false | La barre de titre de la fenêtre n’est pas affichée.      |



 

## <a name="remarks"></a>Remarques

Si la barre de titre est affichée, les boutons zone de contrôle, réduire et fermer s’affichent. Le titre de la fenêtre sera le titre de l’élément d' **affichage** .

Si **TitleBar** a la valeur true et que l’utilisateur tente de modifier la valeur de **Video. Zoom**, la modification ne se produit pas, sauf si l’apparence analyse la **Zoom** et prend la mesure appropriée pour se redimensionner.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément VIEW**](view-element.md)
</dt> <dt>

[**VIEW. title**](view-title.md)
</dt> <dt>

[**VIDEO. Zoom**](video-zoom.md)
</dt> </dl>

 

 





