---
description: La propriété DefaultSubpictureLanguageExt récupère l’extension du langage de sous-image de DVD par défaut.
ms.assetid: bd437844-6e5c-4237-a968-700a53e18635
title: Propriété DefaultSubpictureLanguageExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55dbf4bac4a5fb66e369c67e986c064112826c2184dcd5df1d858235632cba98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102989"
---
# <a name="defaultsubpicturelanguageext-property"></a>Propriété DefaultSubpictureLanguageExt

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DefaultSubpictureLanguageExt` propriété récupère l’extension du langage de sous-image de DVD par défaut.

``` syntax
[ iLangExt = ] MSWebDVD.DefaultSubpictureLanguageExt
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière indiquant l’extension du langage de sous-image de DVD par défaut.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture seule sans valeur par défaut. Le tableau suivant répertorie les valeurs possibles.



| Value | Description                    |
|-------|--------------------------------|
| 0     | Extension non spécifiée        |
| 1     | Légendes normales                |
| 2     | Grandes légendes                   |
| 3     | Légendes des enfants            |
| 5     | Sous-titres normaux         |
| 6     | Légendes volumineuses fermées            |
| 7     | Sous-titres des enfants fermés     |
| 9     | Forcé                         |
| 13    | Commentaires du directeur normal     |
| 14    | Commentaires du grand directeur        |
| 15    | Commentaires Director’s des enfants |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SelectDefaultSubpictureLanguage**](selectdefaultsubpicturelanguage-method.md)
</dt> </dl>

 

 



