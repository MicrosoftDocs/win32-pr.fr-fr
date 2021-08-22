---
title: Player. URL
description: La propriété URL spécifie ou récupère le nom de l’élément multimédia à lire.
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- Lecteur Windows Media Player. URL
topic_type:
- apiref
api_name:
- Player.URL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00a6513350ee9c39855aba8168faf9ced788a0686a0fdbe845013dcc521142f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572038"
---
# <a name="playerurl"></a>Player. URL

La propriété **URL** spécifie ou récupère le nom de l’élément multimédia à lire.

## <a name="syntax"></a>Syntaxe

*lecteur* . **URL**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture/écriture sans valeur par défaut.

## <a name="remarks"></a>Notes

Cette propriété peut uniquement être définie sur une URL dans une zone de sécurité identique ou moins restrictive que la zone de sécurité du programme ou de la page Web appelante.

Les applications qui ouvrent des éléments multimédias à partir d’un pare-feu offrent de meilleures performances si l’adresse est spécifiée à l’aide du nom DNS (Domain Name Server) au lieu de l’adresse IP.

N’appelez pas cette méthode à partir du code du gestionnaire d’événements. Appelant *Player*. L' **URL** d’un gestionnaire d’événements peut produire des résultats inattendus.

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément INPUT de texte HTML et un élément INPUT de bouton HTML. L’élément TEXT permet à l’utilisateur de taper un chemin d’accès pour spécifier un fichier multimédia numérique à lire. l’élément BUTTON exécute JScript qui ouvre le fichier et démarre Lecteur Windows Media. L’objet **Player** a été créé avec ID = "Player".


```JScript
<!-- Create an INPUT control to get a file path from the user. -->
<INPUT Type = "TEXT" ID = "inputURL">

<!-- Create a BUTTON control to execute the script. -->
<INPUT  Type = "BUTTON"  ID = "openMedia"  VALUE = "Open Media"
    onClick = "
        /* Specify the URL obtained from user input. */
        Player.URL = inputURL.value;

        /* Start the Player. */
        Player.controls.play();
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

 

 





