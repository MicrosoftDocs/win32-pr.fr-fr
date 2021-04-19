---
title: AmbientAttributes. passThrough
description: L’attribut passThrough spécifie ou récupère une valeur indiquant si le contrôle passera tous les événements de souris au contrôle situé sous celui-ci.
ms.assetid: 907ae233-3421-4e80-84be-64db4a3ab654
keywords:
- Lecteur Windows Media AmbientAttributes. passThrough
topic_type:
- apiref
api_name:
- AmbientAttributes.passThrough
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b786aeefc182caab904c644dfd00ab4e76fec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545395"
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



 

## <a name="remarks"></a>Notes

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

 

 





