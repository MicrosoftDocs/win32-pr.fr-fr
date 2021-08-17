---
title: Méthode IWMPMediaCollection getByAlbum
description: La méthode getByAlbum retourne une interface IWMPPlaylist qui fournit l’accès aux éléments multimédias à partir de l’album spécifié.
ms.assetid: 26f004c0-de46-4792-8212-9d4ac749bb21
keywords:
- Lecteur Windows Media de la méthode getByAlbum
- méthode getByAlbum Lecteur Windows Media, interface IWMPMediaCollection
- Lecteur Windows Media de l’interface IWMPMediaCollection, méthode getByAlbum
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAlbum
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07137068961447b9f311dbdb765d34fbf2689ca80fd2035e8a60ebe27e4037bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117929762"
---
# <a name="iwmpmediacollectiongetbyalbum-method"></a>IWMPMediaCollection :: getByAlbum, méthode

La méthode **getByAlbum** retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias à partir de l’album spécifié.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPPlaylist getByAlbum(
  System.String bstrAlbum
);
```


```VB

Public Function getByAlbum( _
  ByVal bstrAlbum As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAlbum
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrAlbum* \[ dans\]
</dt> <dd>

**System. String** qui est le titre de l’album.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Interface **wmplib. IWMPPlaylist** pour les éléments multimédias récupérés.

## <a name="remarks"></a>Remarques

Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

Il existe deux façons de récupérer une interface **IWMPMediaCollection** , et le comportement de la méthode **getByAlbum** dépend de ceux de ces deux méthodes. Si vous récupérez l’interface en appelant [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), la méthode **getByAlbum** retourne tous les éléments multimédias de la bibliothèque. Toutefois, si vous récupérez l’interface en appelant [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), la méthode **getByAlbum** retourne uniquement les éléments audio de la bibliothèque qui appartiennent à l’album spécifié.

## <a name="examples"></a>Exemples

L’exemple suivant utilise **getByAlbum** pour créer une sélection d’éléments multimédias lorsque l’utilisateur clique sur un bouton. La sélection contient des éléments avec l’album spécifié par l’utilisateur dans une zone de texte. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void playAlbum_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the album title text that the user entered in the text box. 
    string album = getAlbum.Text;

    // Create the playlist using getByAlbum. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAlbum(album);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAlbum_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAlbum.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the album title text that the user entered in the text box. 
    Dim album As String = getAlbum.Text

    &#39; Create the playlist using getByAlbum. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAlbum(album)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPMediaCollection (VB et C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





