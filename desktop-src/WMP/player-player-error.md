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
ms.openlocfilehash: a99411773994ad012155eea5a203ed341d50b460
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010991"
---
# <a name="playererror-event"></a>Événement Player. Error

L’événement d' **erreur** se produit lorsqu’il y a une condition d’erreur.

## <a name="syntax"></a>Syntaxe


```JScript
Player.Error()
```



## <a name="parameters"></a>Paramètres

Cet événement n’a pas de paramètres.

## <a name="return-value"></a>Valeur de retour

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



## <a name="requirements"></a>Spécifications



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

 

 





