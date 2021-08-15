---
title: Méthode playlist. setItemInfo
description: La méthode setItemInfo spécifie la valeur d’un attribut playlist.
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- Lecteur Windows Media de la méthode setItemInfo
- méthode setItemInfo Lecteur Windows Media, classe Playlist
- Lecteur Windows Media de classe Playlist, méthode setItemInfo
topic_type:
- apiref
api_name:
- Playlist.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47208d1fad03a57e26d1f5591adf658c7553a9087254b49c7aecfd904bd4d95f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335746"
---
# <a name="playlistsetiteminfo-method"></a>Méthode playlist. setItemInfo

La méthode **setItemInfo** spécifie la valeur d’un attribut playlist.

## <a name="syntax"></a>Syntaxe


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom de l’attribut à définir. pour plus d’informations sur les attributs pris en charge par Lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md)Lecteur Windows Media.

</dd> <dt>

*valeur* \[ dans\]
</dt> <dd>

**Chaîne** contenant la nouvelle valeur de l’attribut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Une utilisation spéciale de la méthode **setItemInfo** consiste à trier les éléments de la sélection à l’aide de l’attribut SortAttribute. l’exemple de JScript suivant trie une sélection selon les valeurs de l’attribut UserLastPlayedTime. La sélection de variable est une référence à un objet **playlist** .


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="examples"></a>Exemples

Consultez la propriété [attributeCount](playlist-attributecount.md) pour obtenir un exemple de code qui utilise cette propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet playlist**](playlist-object.md)
</dt> <dt>

[**Playlist. getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





