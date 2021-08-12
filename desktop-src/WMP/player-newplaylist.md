---
title: Player. newPlaylist, méthode
description: La méthode newPlaylist crée un nouvel objet playlist.
ms.assetid: a566006e-8647-4c51-ab77-762728f25a30
keywords:
- Lecteur Windows Media de la méthode newPlaylist
- méthode newPlaylist Lecteur Windows Media, classe Player
- Lecteur Windows Media de classe Player, méthode newPlaylist
topic_type:
- apiref
api_name:
- Player.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 380d1f2751487f5c648b154852be625a5c93103851541dea7e2488ba75080ca0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572829"
---
# <a name="playernewplaylist-method"></a>Player. newPlaylist, méthode

La méthode **newPlaylist** crée un nouvel objet **playlist** .

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Player.newPlaylist(
  name,
  URL
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom de la nouvelle sélection.

</dd> <dt>

*URL* \[ dans\]
</dt> <dd>

**chaîne** contenant l’URL de la sélection de métafichier multimédia Windows pour créer l’objet de **sélection** .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne un objet **playlist** .

## <a name="remarks"></a>Notes

Si le paramètre *URL* a la valeur null ou «» (chaîne vide), un objet **playlist** vide est créé. Si le paramètre *Name* est défini sur «», le nom dans le métafichier est utilisé.

La nouvelle playlist créée avec cette méthode n’est pas ajoutée à la bibliothèque. Pour ajouter une nouvelle sélection à la bibliothèque, utilisez *PlaylistCollection*. **importPlaylist** ou *PlaylistCollection*. **newPlaylist**. Tout espace de début ou de fin dans le nom de la playlist est automatiquement supprimé lorsqu’il est ajouté à la bibliothèque.

Étant donné que la bibliothèque autorise plusieurs sélections portant le même nom, vous souhaiterez peut-être vérifier la présence d’une sélection avec un nom donné avant d’en ajouter une nouvelle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**PlaylistCollection. newPlaylist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Windows Fichiers multimédias**](windows-media-metafiles.md)
</dt> </dl>

 

 





