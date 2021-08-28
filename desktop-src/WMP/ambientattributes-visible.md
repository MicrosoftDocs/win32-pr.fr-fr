---
title: AmbientAttributes. visible
description: L’attribut visible spécifie ou récupère la visibilité du contrôle.
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- AmbientAttributes. visible Lecteur Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6136bbdba7fe222c16e6185bc2ddfa243c5387443122fb93eb1d6564ad01c956
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124049"
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



 

## <a name="remarks"></a>Remarques

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

 

 





