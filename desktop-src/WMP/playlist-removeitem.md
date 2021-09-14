---
title: Playlist. removeItem, méthode
description: La méthode removeItem supprime l’élément spécifié de la sélection.
ms.assetid: 294ba4fb-967b-4a03-b0c5-6e9c15db3bff
keywords:
- removeItem, méthode Lecteur Windows Media
- removeItem, méthode Lecteur Windows Media, classe Playlist
- Lecteur Windows Media de classe Playlist, méthode removeItem
topic_type:
- apiref
api_name:
- Playlist.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de03333e2373744f9e9197be8ed8582997c557d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292979"
---
# <a name="playlistremoveitem-method"></a>Playlist. removeItem, méthode

La méthode **RemoveItem** supprime l’élément spécifié de la sélection.

## <a name="syntax"></a>Syntaxe


```JScript
Playlist.removeItem(
  item
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*élément* \[ dans\]
</dt> <dd>

Objet **multimédia** à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si l’élément supprimé est la piste en cours de lecture (*Player*.**currentMedia**), la lecture s’arrête et l’élément suivant dans la sélection devient l’élément actuel. S’il n’y a pas d’élément suivant, l’élément précédent est utilisé, ou s’il n’y a pas d’autres éléments, alors *Player*. **currentMedia** a la valeur **null**.

Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Objet playlist**](playlist-object.md)
</dt> <dt>

[**Playlist. insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Playlist. Item**](playlist-item.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





