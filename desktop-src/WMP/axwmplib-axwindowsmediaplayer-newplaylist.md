---
title: Méthode AxWindowsMediaPlayer. newPlaylist
description: La méthode newPlaylist renvoie une interface IWMPPlaylist pour une nouvelle sélection.
ms.assetid: caee8ee5-6201-474d-a4cb-80e574f84f0b
keywords:
- méthode newPlaylist lecteur Windows Media
- méthode newPlaylist lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, méthode newPlaylist
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dc82be7aae37b4c1334b79f84e9d607b4f73cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543833"
---
# <a name="axwindowsmediaplayernewplaylist-method"></a>Méthode AxWindowsMediaPlayer. newPlaylist

La méthode newPlaylist renvoie une interface IWMPPlaylist pour une nouvelle sélection.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName,
  System.String bstrURL
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String, _
  ByVal bstrURL As System.String _
) As IWMPPlaylist
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrName,* 
</dt> <dd>

**System. String** qui est le nom de la nouvelle sélection.

</dd> <dt>

*bstrURL* 
</dt> <dd>

**System. String** qui est l’URL de la sélection de métafichiers Windows Media utilisée pour initialiser la nouvelle sélection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Interface WMPLib. IWMPPlaylist qui représente la sélection nouvellement créée.

## <a name="remarks"></a>Notes

Si le paramètre *du bstrURL* est une chaîne null ou de longueur nulle (""), cette méthode crée une **sélection** vide. Si le paramètre *bstrName* est une chaîne de longueur nulle (""), cette méthode applique le nom du métafichier actuel.

La nouvelle playlist créée avec cette méthode n’est pas ajoutée à la bibliothèque. Pour ajouter une nouvelle sélection à la bibliothèque, utilisez IWMPPlaylistCollection. **importPlaylist** ou IWMPPlaylistCollection. **newPlaylist**. Tout espace de début ou de fin dans le nom de la playlist est automatiquement supprimé lorsqu’il est ajouté à la bibliothèque.

Étant donné que la bibliothèque autorise plusieurs sélections portant le même nom, vous souhaiterez peut-être vérifier la présence d’une sélection avec un nom donné avant d’en ajouter une nouvelle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. importPlaylist (VB et C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. newPlaylist (VB et C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





