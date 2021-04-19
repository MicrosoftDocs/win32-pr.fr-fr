---
title: Event. Button
description: L’attribut Button récupère une valeur indiquant les boutons de la souris qui étaient inactifs lorsque l’événement s’est produit.
ms.assetid: 58fb1522-9946-4942-b4bf-4cff37f7dbaf
keywords:
- Event. Button lecteur Windows Media
topic_type:
- apiref
api_name:
- event.button
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f218c0703bd2847cc0f3b7fb2091bbb02e7863e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526337"
---
# <a name="eventbutton"></a>Event. Button

L’attribut **Button** récupère une valeur indiquant les boutons de la souris qui étaient inactifs lorsque l’événement s’est produit.

``` syntax
event.button
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture seule (**long**).



| Valeur | Description                      |
|-------|----------------------------------|
| 0     | Aucun bouton de la souris n’était enfoncé.      |
| 1     | Le bouton gauche de la souris était enfoncé.  |
| 2     | Le bouton droit de la souris était enfoncé. |
| 3     | Les deux boutons de la souris étaient inactifs.    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs d’événement ambiant**](ambient-event-attributes.md)
</dt> </dl>

 

 





