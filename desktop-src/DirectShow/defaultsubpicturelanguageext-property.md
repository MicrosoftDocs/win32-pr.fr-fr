---
description: La propriété DefaultSubpictureLanguageExt récupère l’extension du langage de sous-image de DVD par défaut.
ms.assetid: bd437844-6e5c-4237-a968-700a53e18635
title: Propriété DefaultSubpictureLanguageExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37bba455a26df4eaa6676b77447c3faed408609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520748"
---
# <a name="defaultsubpicturelanguageext-property"></a>Propriété DefaultSubpictureLanguageExt

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DefaultSubpictureLanguageExt` propriété récupère l’extension du langage de sous-image de DVD par défaut.

``` syntax
[ iLangExt = ] MSWebDVD.DefaultSubpictureLanguageExt
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière indiquant l’extension du langage de sous-image de DVD par défaut.

## <a name="remarks"></a>Notes

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

 

 



