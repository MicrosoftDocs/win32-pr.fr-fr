---
title: Événement Player. OpenStateChange
description: L’événement OpenStateChange se produit lorsque la propriété openState change de valeur. | Événement Player. OpenStateChange
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- Événement OpenStateChange lecteur Windows Media
- Événement OpenStateChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement OpenStateChange
topic_type:
- apiref
api_name:
- Player.OpenStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020a25a811623b9f7d7dd8f316c470cada6a142b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540392"
---
# <a name="playeropenstatechange-event"></a>Événement Player. OpenStateChange

L’événement **OpenStateChange** se produit lorsque la propriété **openState** change de valeur.

## <a name="syntax"></a>Syntaxe


```JScript
Player.OpenStateChange(
  NewState
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NewState* 
</dt> <dd>

**Nombre** (**long**) spécifiant le nouvel état ouvert. Consultez [openState](player-openstate.md) pour obtenir une table de valeurs.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le lecteur Windows Media peut passer par plusieurs États ouverts pendant qu’il tente d’ouvrir un fichier réseau, par exemple Rechercher le serveur, se connecter au serveur et enfin ouvrir le fichier. Cet événement est déclenché chaque fois que l’état ouvert change.

La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

Il n’est pas garanti que les États du lecteur Windows Media se produisent dans un ordre particulier. En outre, tous les États ne se produisent pas nécessairement au cours d’une séquence d’événements. Vous ne devez pas écrire du code qui s’appuie sur l’ordre de l’État.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**Player. openState**](player-openstate.md)
</dt> </dl>

 

 





