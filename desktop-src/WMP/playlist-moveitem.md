---
title: Méthode playlist. moveItem
description: La méthode moveItem modifie l’emplacement d’un élément dans la sélection.
ms.assetid: 82a8de86-4419-48a7-89f8-f7b9084b51d4
keywords:
- méthode moveItem lecteur Windows Media
- méthode moveItem lecteur Windows Media, classe de sélection
- Classe de sélection lecteur Windows Media, méthode moveItem
topic_type:
- apiref
api_name:
- Playlist.moveItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e2e48b2987af4becd8c07357ff2eecf137f31d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537659"
---
# <a name="playlistmoveitem-method"></a>Méthode playlist. moveItem

La méthode **moveItem** modifie l’emplacement d’un élément dans la sélection.

## <a name="syntax"></a>Syntaxe


```JScript
Playlist.moveItem(
  oldIndex,
  newIndex
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*OldIndex* \[ dans\]
</dt> <dd>

**Nombre** (**long**) contenant l’ancien index.

</dd> <dt>

*NewIndex* \[ dans\]
</dt> <dd>

**Nombre** (**long**) contenant le nouvel index.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Les sélections stockées dans la bibliothèque peuvent changer en dehors de votre contrôle. Veillez à surveiller et à gérer tous les événements appropriés liés à la sélection afin que l’ordre des éléments dans la sélection ne change pas de manière inattendue.

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

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





