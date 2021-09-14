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
ms.openlocfilehash: b6144f6e1cfda93be32060e8206a96b0da7568d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404131"
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

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un objet **playlist** .

## <a name="remarks"></a>Notes

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Spécifications



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

 

 





