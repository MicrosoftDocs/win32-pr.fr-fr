---
title: Player. Buffering (événement)
description: L’événement de mise en mémoire tampon se produit lorsque le contrôle du lecteur Windows Media démarre ou termine la mise en mémoire tampon ou le téléchargement. | Player. Buffering (événement)
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- Mise en mémoire tampon des événements Windows Media Player
- Événement de mise en mémoire tampon Windows Media Player, classe Player
- Classe de lecteur Windows Media Player, événement de mise en mémoire tampon
topic_type:
- apiref
api_name:
- Player.Buffering
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a73ac77f9b8e81162a6cc0f9220562caba26eae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526049"
---
# <a name="playerbuffering-event"></a>Player. Buffering (événement)

L’événement de **mise en mémoire tampon** se produit lorsque le contrôle du lecteur Windows Media démarre ou termine la mise en mémoire tampon ou le téléchargement.

## <a name="syntax"></a>Syntaxe


```JScript
Player.Buffering(
  Start
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Start* 
</dt> <dd>

**Valeur booléenne** contenant l’une des valeurs suivantes.



| Valeur | Description            |
|-------|------------------------|
| true  | La mise en mémoire tampon a démarré. |
| false | La mise en mémoire tampon s’est terminée.   |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Utilisez cet événement pour déterminer quand la mise en mémoire tampon ou le téléchargement démarre ou s’arrête. Vous pouvez utiliser le même bloc d’événements pour les cas et le *réseau* de test. **bufferingProgress** et *réseau*. **downloadProgress** pour déterminer si le lecteur Windows Media met actuellement en mémoire tampon ou télécharge le contenu.

La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé en utilisant le nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Network. bufferingProgress**](network-bufferingprogress.md)
</dt> <dt>

[**Network. downloadProgress**](network-downloadprogress.md)
</dt> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





