---
title: Playlist. insertItem, méthode
description: La méthode insertItem insère un élément multimédia dans la sélection à l’emplacement spécifié.
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- méthode insertItem Lecteur Windows Media
- méthode insertItem Lecteur Windows Media, classe Playlist
- Lecteur Windows Media de classe Playlist, méthode insertItem
topic_type:
- apiref
api_name:
- Playlist.insertItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a456b7a359d59958ce7693cc48c16eabba435621
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293006"
---
# <a name="playlistinsertitem-method"></a>Playlist. insertItem, méthode

La méthode **InsertItem** insère un élément multimédia dans la sélection à l’emplacement spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

**Nombre** (**long**) contenant l’index auquel ajouter l’élément.

</dd> <dt>

*élément* \[ dans\]
</dt> <dd>

Objet **multimédia** à insérer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Tous les éléments après l’élément inséré auront leurs numéros d’index augmentés d’une unité.

Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet playlist**](playlist-object.md)
</dt> <dt>

[**Playlist. Item**](playlist-item.md)
</dt> <dt>

[**Playlist. removeItem**](playlist-removeitem.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





