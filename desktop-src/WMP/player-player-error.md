---
title: Événement Player. Error
description: L’événement d’erreur se produit lorsqu’il y a une condition d’erreur.
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- Lecteur Windows Media d’événement d’erreur
- événement d’erreur Lecteur Windows Media, classe Player
- Lecteur Windows Media de classe Player, événement d’erreur
topic_type:
- apiref
api_name:
- Player.Error
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a7e4642eef19b4edc4b1aa5bc75022a307d279d0d60482af0c7e2f0a9368c06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134812"
---
# <a name="playererror-event"></a>Événement Player. Error

L’événement d' **erreur** se produit lorsqu’il y a une condition d’erreur.

## <a name="syntax"></a>Syntaxe


```JScript
Player.Error()
```



## <a name="parameters"></a>Paramètres

Cet événement n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant crée un gestionnaire d’événements pour afficher le texte de description de la première erreur dans la file d’attente d’erreurs. L’objet **Player** a été créé avec ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the description of the first error. 
var errDesc = Player.error.item(0).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ErrorItem. errorDescription**](erroritem-errordescription.md)
</dt> <dt>

[**Erreur. élément**](error-item.md)
</dt> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





