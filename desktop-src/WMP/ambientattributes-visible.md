---
title: AmbientAttributes. visible
description: L’attribut visible spécifie ou récupère la visibilité du contrôle.
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- Lecteur Windows Media AmbientAttributes. visible
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72794b7bbba0237a687dc70bda761c505b839e59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526400"
---
# <a name="ambientattributesvisible"></a>AmbientAttributes. visible

L’attribut **visible** spécifie ou récupère la visibilité du contrôle.

``` syntax
        elementID.visible
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                      |
|-------|----------------------------------|
| true  | Par défaut. Le contrôle est visible. |
| false | Le contrôle n'est pas visible.      |



 

## <a name="remarks"></a>Notes

Cet attribut est utile pour masquer des contrôles, par exemple lors du remplacement d’un bouton de pause pour un bouton de lecture.

Si la valeur est false, le contrôle n’est pas visible et les événements de clic sont passés au contrôle situé derrière lui. Si la valeur est true, le contrôle est visible et reçoit l’événement Click lui-même.

La valeur par défaut de l’élément **automenu** est false.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> </dl>

 

 





