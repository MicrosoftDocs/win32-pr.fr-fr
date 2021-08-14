---
title: BUTTONGROUP. showBackground
description: L’attribut showBackground spécifie ou récupère une valeur indiquant si le BUTTONGROUP affiche uniquement les boutons, ou affiche la bitmap complète spécifiée dans l’attribut image.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- BUTTONGROUP. showBackground Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb95b707fa7e14b00e86c5a65949ff9fba3ce3db32745116fa65ca4c53ac1998
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342672"
---
# <a name="buttongroupshowbackground"></a>BUTTONGROUP. showBackground

L’attribut **showBackground** spécifie ou récupère une valeur indiquant si le **BUTTONGROUP** affiche uniquement les boutons, ou affiche la bitmap complète spécifiée dans l’attribut **image** .

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| true  | Les boutons s’affichent et la zone non occupée par les boutons est dessinée à partir de l’image bitmap. |
| false | Par défaut. Seuls les boutons s’affichent.                                                   |



 

## <a name="remarks"></a>Remarques

Quand **showBackground** a la valeur true, la totalité de l' **image** principale est visible.

Quand **showBackground** a la valeur false, seules les zones correspondant aux couleurs **mappingImage** affectées seront rendues. En d’autres termes, seuls les **BUTTONELEMENTs** avec le **mappingColor** affecté sont visibles.

Si une valeur non valide est spécifiée, l’état précédent est conservé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONELEMENT. mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**BUTTONGROUP. image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP. mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





