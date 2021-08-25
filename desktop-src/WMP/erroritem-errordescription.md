---
title: ErrorItem. errorDescription
description: La propriété errorDescription récupère une description de l’erreur.
ms.assetid: 7fd16c3d-1460-41b5-81ca-2636d7a1d0d1
keywords:
- ErrorItem. errorDescription Lecteur Windows Media
topic_type:
- apiref
api_name:
- ErrorItem.errorDescription
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5740adcef0b6eb86290ea392d0659abb0ccc3d51b0b0b1b3203105de67fb692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862789"
---
# <a name="erroritemerrordescription"></a>ErrorItem. errorDescription

La propriété **errorDescription** récupère une description de l’erreur.

``` syntax
player.error.item(
        index
        ).errorDescription
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule.

## <a name="remarks"></a>Remarques

vous devez définir *Paramètres*. **enableErrorDialogs** sur false si vous choisissez d’afficher des messages d’erreur personnalisés.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise *ErrorItem*. **errorDescription** dans un gestionnaire d’événements pour afficher le message d’erreur à l’utilisateur. L’objet **Player** a été créé avec ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error description for the first error item.
errDesc = Player.error.item(0).errorDescription;

// Display the error code.
var message = "Error: " + errDesc";
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





