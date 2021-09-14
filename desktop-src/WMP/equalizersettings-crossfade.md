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
ms.openlocfilehash: 0472f90f94b5c4ba56948848476b6585502427c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191775"
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



 

## <a name="remarks"></a>Notes

La fondu enchaîné est une fonctionnalité de traitement audio qui diminue progressivement le volume d’un élément multimédia près de la fin de sa lecture tout en démarrant simultanément la lecture de l’élément multimédia suivant au niveau du volume minimum et en l’accroissant progressivement au volume normal. Le chevauchement entre le début du deuxième élément multimédia et la fin du premier élément multimédia est spécifié par l’attribut **crossFadeWindow** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.crossFadeWindow**](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





