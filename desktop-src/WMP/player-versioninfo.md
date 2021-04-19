---
title: Player. versionInfo
description: La propriété versionInfo récupère une valeur de chaîne spécifiant la version du lecteur Windows Media.
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
ms.openlocfilehash: b44a94fa2df6d5e7d46108ec971fd84481688eb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535945"
---
# <a name="playerversioninfo"></a>Player. versionInfo

La propriété **VERSIONINFO** récupère une valeur de chaîne spécifiant la version du lecteur Windows Media.

## <a name="syntax"></a>Syntaxe

*lecteur* . **VERSIONINFO**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule au format suivant : «*X*. 0,0. *Yyyy*"où *X* représente le numéro de version principale et *yyyy* représente le numéro de Build.

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément bouton HTML qui, lorsque vous cliquez dessus, affiche une boîte de message contenant les informations de version pour le lecteur Windows Media. L’objet **Player** a été créé avec ID = "Player".


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

 

 





