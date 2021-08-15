---
title: PlaylistArray. Item, méthode
description: La méthode Item récupère la sélection à l’index donné.
ms.assetid: cc851695-f9a2-4594-8bd3-3555c18bfa10
keywords:
- méthode item Lecteur Windows Media
- méthode item Lecteur Windows Media, classe PlaylistArray
- Lecteur Windows Media de la classe PlaylistArray, méthode item
topic_type:
- apiref
api_name:
- PlaylistArray.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a45bb38250285563d9e4b7abcc1a4bfd1f7a0bea35b41b7e4cd801f8eff1d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335426"
---
# <a name="playlistarrayitem-method"></a>PlaylistArray. Item, méthode

La méthode **Item** récupère la sélection à l’index donné.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = PlaylistArray.item(
  index
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

**Nombre** (**long**) contenant l’index de la sélection à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **playlist** .

## <a name="remarks"></a>Remarques

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





