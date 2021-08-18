---
title: Player. versionInfo
description: la propriété versionInfo récupère une valeur de chaîne qui spécifie la version de la Lecteur Windows Media.
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- Lecteur Windows Media Player. versionInfo
topic_type:
- apiref
api_name:
- Player.versionInfo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2251d610ad8a522155e37c8d416123c9d09faef5da2b4af4da75aeb745940f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995829"
---
# <a name="playerversioninfo"></a>Player. versionInfo

la propriété **versionInfo** récupère une valeur de chaîne qui spécifie la version de la Lecteur Windows Media.

## <a name="syntax"></a>Syntaxe

*lecteur* . **VERSIONINFO**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule au format suivant : «*X*. 0,0. *Yyyy*"où *X* représente le numéro de version principale et *yyyy* représente le numéro de Build.

## <a name="examples"></a>Exemples

l’exemple suivant crée un élément bouton HTML qui, lorsque vous cliquez dessus, affiche une boîte de message contenant les informations de version de Lecteur Windows Media. L’objet **Player** a été créé avec ID = "Player".


```
<INPUT TYPE = "BUTTON"  ID = "VERSION"  VALUE = "Show Version"
    onClick = "
        /* Build the message containing the version info. */
        var message = 'Windows Media Player Version: ';
        message += '\n';
        message += Player.versionInfo;
 
        /* Display the message box. */
        alert(message);
">

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





