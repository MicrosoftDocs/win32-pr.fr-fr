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
ms.openlocfilehash: 7a71d9ceb39b29c1627ea7596166c39b3dc2f6c76faf45e5ffb54bea14154ac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995699"
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

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Tous les éléments après l’élément inséré auront leurs numéros d’index augmentés d’une unité.

Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Configuration requise



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

 

 





