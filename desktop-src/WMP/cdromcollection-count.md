---
title: CdromCollection. Count
description: La propriété Count récupère le nombre de lecteurs de CD et de DVD disponibles sur le système.
ms.assetid: 98d24713-6a55-409f-af9a-fc941ad6d8f5
keywords:
- CdromCollection. Count lecteur Windows Media
topic_type:
- apiref
api_name:
- CdromCollection.count
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf7150ca31caaf68fa51ae42fded223d24a8e59f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526463"
---
# <a name="cdromcollectioncount"></a>CdromCollection. Count

La propriété **Count** récupère le nombre de lecteurs de CD et de DVD disponibles sur le système.

``` syntax
player.cdromCollection.count
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="remarks"></a>Notes

Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

Les lecteurs de DVD-ROM sont comptés exactement comme les lecteurs de CD. Toutefois, le contrôle du lecteur Windows Media ne prend en charge que les fonctionnalités DVD pour Windows XP ou les systèmes d’exploitation ultérieurs. En règle générale, les lecteurs de DVD peuvent lire des CD, mais les lecteurs de CD ne peuvent pas lire les DVD.

**Lecteur Windows Media 10 Mobile :** Cette méthode retourne toujours 0.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise *CdromCollection*. **nombre** pour afficher le nombre de lecteurs de CD et de DVD disponibles sur l’ordinateur de l’utilisateur. L’objet Player a été créé avec ID = "Player".


```JScript
// Store the count of drives found on the computer.
var numCDROMS = Player.cdromCollection.count;

// Build the string to display to the user.
var displayString = numCDROMS + " drive(s) found.";

// Show a message box with the count information.
alert(displayString);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet CdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





