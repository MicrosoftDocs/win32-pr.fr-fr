---
title: Player. Buffering (événement)
description: l’événement de mise en mémoire tampon se produit lorsque le contrôle Lecteur Windows Media commence ou termine la mise en mémoire tampon ou le téléchargement. | Player. Buffering (événement)
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- Lecteur Windows Media d’événement de mise en mémoire tampon
- Lecteur Windows Media d’événement de mise en mémoire tampon, classe Player
- Lecteur Windows Media de classe Player, événement de mise en mémoire tampon
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292546"
---
# <a name="playerbuffering-event"></a>Player. Buffering (événement)

l’événement de **mise en mémoire tampon** se produit lorsque le contrôle Lecteur Windows Media commence ou termine la mise en mémoire tampon ou le téléchargement.

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

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Utilisez cet événement pour déterminer quand la mise en mémoire tampon ou le téléchargement démarre ou s’arrête. Vous pouvez utiliser le même bloc d’événements pour les cas et le *réseau* de test. **bufferingProgress** et *réseau*. **downloadProgress** pour déterminer si Lecteur Windows Media est en train de mettre en mémoire tampon ou de télécharger du contenu.

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

## <a name="requirements"></a>Spécifications



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

 

 





