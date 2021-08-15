---
title: EQUALIZERSETTINGS. fondu enchaîné
description: L’attribut fondu enchaîné spécifie ou récupère une valeur indiquant si le fondu croisé est activé.
ms.assetid: 6c5a31f3-982e-4660-80ff-30b7a4290a15
keywords:
- EQUALIZERSETTINGS. fondu enchaîné Lecteur Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.crossFade
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff38ee7634f31da7717bfca015ebaacd88796d9c8186faef155704a449bbb07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118838624"
---
# <a name="equalizersettingscrossfade"></a>EQUALIZERSETTINGS. fondu enchaîné

L’attribut **fondu enchaîné** spécifie ou récupère une valeur indiquant si le fondu croisé est activé.

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                      |
|-------|----------------------------------|
| true  | Le fondu croisé est activé.           |
| false | Par défaut. Le fondu croisé est désactivé. |



 

## <a name="remarks"></a>Remarques

La fondu enchaîné est une fonctionnalité de traitement audio qui diminue progressivement le volume d’un élément multimédia près de la fin de sa lecture tout en démarrant simultanément la lecture de l’élément multimédia suivant au niveau du volume minimum et en l’accroissant progressivement au volume normal. Le chevauchement entre le début du deuxième élément multimédia et la fin du premier élément multimédia est spécifié par l’attribut **crossFadeWindow** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.crossFadeWindow**](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





