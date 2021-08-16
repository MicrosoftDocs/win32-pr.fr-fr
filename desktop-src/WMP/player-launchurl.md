---
title: Player. launchURL, méthode
description: La méthode launchURL envoie une URL au navigateur par défaut de l’utilisateur à restituer. | Player. launchURL, méthode
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- Lecteur Windows Media de la méthode launchURL
- méthode launchURL Lecteur Windows Media, classe Player
- Lecteur Windows Media de classe Player, méthode launchURL
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
ms.openlocfilehash: 79d22c65a29aaee9c849677dfa42acb5769bf30d2fb7079e305ee79632ef22e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134822"
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

## <a name="remarks"></a>Remarques

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

 

 





