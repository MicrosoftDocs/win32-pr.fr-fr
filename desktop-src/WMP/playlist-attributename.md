---
title: Playlist. attributeName
description: La propriété attributeName récupère le nom d’un attribut au niveau d’un index spécifié.
ms.assetid: 3ff68e78-5fa1-4ca6-aa59-4752dbaee52a
keywords:
- Playlist. attributeName Lecteur Windows Media
topic_type:
- apiref
api_name:
- Playlist.attributeName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 695e0ee00aca0fe7743a028e0e7830e1839c0b2f89b42a94e9ce1dbe29ef35ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003209"
---
# <a name="playlistattributename"></a>Playlist. attributeName

La propriété **AttributeName** récupère le nom d’un attribut au niveau d’un index spécifié.

## <a name="syntax"></a>Syntaxe

*lecteur*. *currentPlaylist*. **AttributeName**( *index* )

## <a name="parameters"></a>Paramètres

*index*

**Nombre** (**long**) contenant l’index.

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule.

## <a name="remarks"></a>Remarques

Le nombre d’attributs est récupéré par la propriété **attributeCount** . Avec un index donné, **AttributeName** retourne une **chaîne** qui peut être utilisée conjointement avec **setItemInfo** ou **getItemInfo** pour spécifier ou récupérer une valeur pour l’attribut.

Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

pour plus d’informations sur les attributs pris en charge par Lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md)Lecteur Windows Media.

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

[**Playlist. attributeCount**](playlist-attributecount.md)
</dt> <dt>

[**Playlist. getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Playlist. setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





