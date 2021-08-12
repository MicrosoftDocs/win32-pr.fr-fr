---
title: ErrorItem. errorCode
description: La propriété errorCode récupère le code d’erreur actuel.
ms.assetid: 1495ec34-0995-40c6-bfd0-f3695784e057
keywords:
- ErrorItem. errorCode Lecteur Windows Media
topic_type:
- apiref
api_name:
- ErrorItem.errorCode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f426bbaf1092b64cdb3578cb681282c9b27d9d2e2e23a69d50f9c065353ad104
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118577703"
---
# <a name="erroritemerrorcode"></a>ErrorItem. errorCode

La propriété **ErrorCode** récupère le code d’erreur actuel.

``` syntax
player.error.item(
        index
        ).errorCode
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="remarks"></a>Notes

vous devez définir *Paramètres*. **enableErrorDialogs** sur false si vous choisissez d’afficher des messages d’erreur personnalisés.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise *ErrorItem*. **ErrorCode** dans un gestionnaire d’événements pour afficher le code d’erreur à l’utilisateur. L’objet **Player** a été créé avec ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error code for the first error item.
errNum = Player.error.item(0).errorCode;

// Display the error information.
var message = "Error number: " + errNum);
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet ErrorItem**](erroritem-object.md)
</dt> <dt>

[**ErrorItem. errorDescription**](erroritem-errordescription.md)
</dt> </dl>

 

 





