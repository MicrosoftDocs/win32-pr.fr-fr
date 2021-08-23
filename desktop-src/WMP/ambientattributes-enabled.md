---
title: AmbientAttributes. Enabled
description: L’attribut enabled spécifie ou récupère une valeur indiquant si le contrôle est activé ou désactivé.
ms.assetid: cf96ab7c-8acd-42b6-b7ca-d084a89c97e2
keywords:
- AmbientAttributes. enabled Lecteur Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.enabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9d8e000d64ef92212cd7c6cf37c7fd79036107e1d3be0d7669d73b40c759de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055177"
---
# <a name="ambientattributesenabled"></a>AmbientAttributes. Enabled

L’attribut **Enabled** spécifie ou récupère une valeur indiquant si le contrôle est activé ou désactivé.

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description               |
|-------|---------------------------|
| true  | Par défaut. Contrôle activé. |
| false | Contrôle désactivé.         |



 

## <a name="remarks"></a>Remarques

Si le contrôle est activé, il peut avoir un taquet de tabulation et recevra tous les événements ambiants. Quand elle est désactivée, le contrôle n’a pas de taquet de tabulation et ne reçoit aucun événement de souris ou de clavier ambiant déclenché. (Toutefois, il continuera à recevoir tous les autres événements ambiants qui lui sont déclenchés.)

Cet attribut n’est pas pris en charge pour l’élément **subview** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> </dl>

 

 





