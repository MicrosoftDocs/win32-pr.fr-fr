---
title: Méthode IWMPMediaCollection getByGenre
description: La méthode getByGenre retourne une interface IWMPPlaylist qui fournit l’accès aux éléments multimédias du genre spécifié.
ms.assetid: 0681e5a2-b56d-4c33-95ce-d9ef3cd5473d
keywords:
- Lecteur Windows Media de la méthode getByGenre
- méthode getByGenre Lecteur Windows Media, interface IWMPMediaCollection
- Lecteur Windows Media de l’interface IWMPMediaCollection, méthode getByGenre
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByGenre
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72f20182f2bfb3bef0d4de2907165a571009072d234add3b8f89ae2db859c7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053597"
---
# <a name="iwmpmediacollectiongetbygenre-method"></a>IWMPMediaCollection :: getByGenre, méthode

La `getByGenre` méthode retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias du genre spécifié.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPPlaylist getByGenre(
  System.String bstrGenre
);
```


```VB

Public Function getByGenre( _
  ByVal bstrGenre As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByGenre
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrGenre* \[ dans\]
</dt> <dd>

**System. String** qui est le nom du genre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Interface **wmplib. IWMPPlaylist** pour les éléments multimédias récupérés.

## <a name="remarks"></a>Remarques

Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

Il existe deux façons de récupérer une interface **IWMPMediaCollection** , et le comportement de la `getByGenre` méthode dépend de ce que vous utilisez pour ces deux méthodes. Si vous récupérez l’interface en appelant [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), la `getByGenre` méthode retourne tous les éléments multimédias de la bibliothèque. Toutefois, si vous récupérez l’interface en appelant [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), la `getByGenre` méthode retourne uniquement les éléments audio de la bibliothèque qui ont l’attribut et la valeur spécifiés.

## <a name="examples"></a>Exemples

L’exemple suivant utilise `getByGenre` pour récupérer une sélection d’éléments multimédias lorsque l’utilisateur clique sur un bouton. La sélection contient des éléments dont le genre est spécifié par l’utilisateur dans une zone de texte. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void playGenre_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the genre that the user entered in the text box. 
    string genre = getGenre.Text;

    // Create the playlist using getByGenre. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByGenre(genre);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playGenre.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the genre that the user entered in the text box. 
    Dim genre As String = getGenre.Text

    &#39; Create the playlist using getByGenre. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByGenre(genre)

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

 

 





