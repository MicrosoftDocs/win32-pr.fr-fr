---
title: Error. clearErrorQueue, méthode
description: La méthode clearErrorQueue efface les erreurs de la file d’attente des erreurs. | Error. clearErrorQueue, méthode
ms.assetid: 306f0700-88b1-4433-8abb-7d225e82060a
keywords:
- méthode clearErrorQueue lecteur Windows Media
- méthode clearErrorQueue lecteur Windows Media, classe d’erreur
- Classe d’erreur lecteur Windows Media, méthode clearErrorQueue
topic_type:
- apiref
api_name:
- Error.clearErrorQueue
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b756708b8f0643f86489c26dd921e87c408be8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522795"
---
# <a name="errorclearerrorqueue-method"></a>Error. clearErrorQueue, méthode

La méthode **clearErrorQueue** efface les erreurs de la file d’attente des erreurs.

## <a name="syntax"></a>Syntaxe


```JScript
Error.clearErrorQueue()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode est utile pour effacer la file d’attente d’erreurs après le traitement d’une série d’erreurs.

Vous devez définir des *paramètres*. **enableErrorDialogs** sur false si vous choisissez d’afficher des messages d’erreur personnalisés.

## <a name="examples"></a>Exemples

L’exemple JScript suivant utilise une *erreur*. **clearErrorQueue** dans un gestionnaire d’événements pour vider la file d’attente d’erreurs après l’affichage de toutes les descriptions d’erreur. L’objet **Player** a été créé avec ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount 

// Loop through the list of errors.
for (var i = 0; i < max; i++){
    // Get the error description for this item.
    var errDesc = Player.error.item(i).errorDescription;
    
    // Display the error message.
    alert(errDesc);
}

// Clear the error queue to prepare for the next group of errors.
Player.error.clearErrorQueue();

</SCRIPT>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Error, objet**](error-object.md)
</dt> </dl>

 

 





