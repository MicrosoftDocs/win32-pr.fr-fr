---
title: Player. launchURL, méthode
description: La méthode launchURL envoie une URL au navigateur par défaut de l’utilisateur à restituer. | Player. launchURL, méthode
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- méthode launchURL lecteur Windows Media
- méthode launchURL lecteur Windows Media, classe Player
- Classe player lecteur Windows Media, méthode launchURL
topic_type:
- apiref
api_name:
- Player.launchURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c496e8f40f4d7c8a21e718b820e438d3ce32ad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527296"
---
# <a name="playerlaunchurl-method"></a>Player. launchURL, méthode

La méthode **launchURL** envoie une URL au navigateur par défaut de l’utilisateur à restituer.

## <a name="syntax"></a>Syntaxe


```JScript
Player.launchURL(
  URL
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*URL* \[ dans\]
</dt> <dd>

Valeur de **chaîne** représentant l’URL à lancer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode ouvre uniquement les pages Web à l’aide des protocoles HTTP ou HTTPs.

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément bouton HTML qui, lorsque vous cliquez dessus, affiche le site Web Microsoft dans une nouvelle fenêtre de navigateur. L’élément **Player** a été créé avec ID = "Player".


```JScript
<INPUT  TYPE = "BUTTON"  ID = "GOTOMS"  VALUE = "Microsoft.com"  onClick = "

    /* Open the Microsoft website. */
    Player.launchURL('https://www.microsoft.com');
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

 

 





