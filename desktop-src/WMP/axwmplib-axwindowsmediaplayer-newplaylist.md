---
title: Méthode AxWindowsMediaPlayer. newPlaylist
description: La méthode newPlaylist renvoie une interface IWMPPlaylist pour une nouvelle sélection.
ms.assetid: caee8ee5-6201-474d-a4cb-80e574f84f0b
keywords:
- Lecteur Windows Media de la méthode newPlaylist
- méthode newPlaylist Lecteur Windows Media, classe AxWindowsMediaPlayer
- Lecteur Windows Media de la classe AxWindowsMediaPlayer, méthode newPlaylist
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
ms.openlocfilehash: f35bbc1d1c8a0f1f76d685676e08119b659ad119176036ab377f9525ce1ab0e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123889"
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

**System. String** qui est l’URL de la sélection de métafichier multimédia Windows qui est utilisée pour initialiser la nouvelle sélection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Interface WMPLib. IWMPPlaylist qui représente la sélection nouvellement créée.

## <a name="remarks"></a>Remarques

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

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. importPlaylist (VB et C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. newPlaylist (VB et C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





