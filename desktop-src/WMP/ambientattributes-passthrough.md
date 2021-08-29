---
title: AmbientAttributes. passThrough
description: L’attribut passThrough spécifie ou récupère une valeur indiquant si le contrôle passera tous les événements de souris au contrôle situé sous celui-ci.
ms.assetid: 907ae233-3421-4e80-84be-64db4a3ab654
keywords:
- AmbientAttributes. passThrough Lecteur Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.passThrough
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e71e9f7a56f7aa103e64ce739c34467f64cde2edb213c37d2d452b506dc5e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055002"
---
# <a name="ambientattributespassthrough"></a>AmbientAttributes. passThrough

L’attribut **passThrough** spécifie ou récupère une valeur indiquant si le contrôle passera tous les événements de souris au contrôle situé sous celui-ci.

``` syntax
        elementID.passThrough
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                            |
|-------|--------------------------------------------------------|
| true  | Le contrôle passe des événements au contrôle situé sous celui-ci. |
| false | Par défaut. Le contrôle ne passe pas d’événements via.         |



 

## <a name="remarks"></a>Remarques

Cet attribut est utile si, par exemple, un contrôle de texte se trouve au-dessus d’un contrôle de bouton uniquement pour fournir une étiquette. Dans ce cas, les clics sur le contrôle de texte doivent être passés au contrôle bouton.

L’attribut **passThrough** n’est pas pris en charge par les éléments **VIEW**, **subview** et **playlist** . Elle ne fonctionnera pas avec l’élément **vidéo** si vous utilisez la *vidéo*. **sans fenêtre** est défini sur false, ni avec l’élément **Effects** si *Effects*. **Windowed** a la valeur true.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> </dl>

 

 





