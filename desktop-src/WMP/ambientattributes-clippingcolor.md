---
title: AmbientAttributes.clippingColor
description: L’attribut clippingColor spécifie ou récupère la couleur à découper de la bitmap clippingImage.
ms.assetid: d6ea43d3-c118-43d3-bfdc-29ddd6ea4978
keywords:
- AmbientAttributes. clippingColor Lecteur Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad526eb0f705d1fce95f3813a666420b29db9de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856185"
---
# <a name="ambientattributesclippingcolor"></a>AmbientAttributes.clippingColor

L’attribut **clippingColor** spécifie ou récupère la couleur à découper de la bitmap **clippingImage** .

``` syntax
        elementID.clippingColor
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.



| Valeur                                       | Description                                       |
|---------------------------------------------|---------------------------------------------------|
| Auto                                        | Par défaut. La couleur de l’emplacement de pixel 0 est utilisée. |
| toute valeur de couleur Microsoft Internet Explorer | La couleur Internet Explorer spécifiée est utilisée.    |



 

## <a name="remarks"></a>Notes

La couleur de découpage indique les régions du **clippingImage** (ou **BackgroundImage** pour la **vue** ou la sous- **vue**) qui correspondent à des portions transparentes et non intercliquables du contrôle. La couleur de découpage peut indiquer plusieurs régions à découper. Un avertissement est émis si **clippingImage** est un jpg pour signaler une perte de couleur dans jpgs.

L’attribut **clippingColor** n’est pas pris en charge par l’élément **playlist** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.clippingImage**](ambientattributes-clippingimage.md)
</dt> <dt>

[**Référence de couleur**](color-reference.md)
</dt> </dl>

 

 





