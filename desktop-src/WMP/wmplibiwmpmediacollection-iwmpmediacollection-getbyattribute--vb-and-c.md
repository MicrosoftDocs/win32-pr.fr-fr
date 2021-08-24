---
title: Méthode IWMPMediaCollection getByAttribute
description: La méthode getByAttribute retourne une interface IWMPPlaylist qui correspond à l’attribut spécifié ayant la valeur spécifiée.
ms.assetid: ece70a2c-38bc-4652-8319-efcde5f9720a
keywords:
- Lecteur Windows Media de la méthode getByAttribute
- méthode getByAttribute Lecteur Windows Media, interface IWMPMediaCollection
- Lecteur Windows Media de l’interface IWMPMediaCollection, méthode getByAttribute
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAttribute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fb8dab44cd1f26c080d438c15f545c882d2e4427af7fa04049b539ce8b3cf13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119735019"
---
# <a name="iwmpmediacollectiongetbyattribute-method"></a>IWMPMediaCollection :: getByAttribute, méthode

La méthode **getByAttribute** retourne une interface **IWMPPlaylist** qui correspond à l’attribut spécifié ayant la valeur spécifiée.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPPlaylist getByAttribute(
  System.String bstrAttribute,
  System.String bstrValue
);
```


```VB

Public Function getByAttribute( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAttribute
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrAttribute* \[ dans\]
</dt> <dd>

**System. String** qui est l’attribut spécifié.

</dd> <dt>

*bstrValue* \[ dans\]
</dt> <dd>

**System. String** qui correspond à la valeur spécifiée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Interface **wmplib. IWMPPlaylist** pour les éléments multimédias récupérés.

## <a name="remarks"></a>Remarques

Cette méthode peut être utilisée pour créer une requête générique pour les éléments multimédias qui correspondent à une valeur pour un attribut de la bibliothèque. Cela est utile dans le cas des attributs définis par l’utilisateur. Si l’attribut n’existe pas, une erreur se produit.

Vous pouvez utiliser cette méthode pour récupérer tous les éléments multimédias d’un type spécifique. Utilisez le nom d’attribut **MediaType** et l’une des valeurs suivantes.



| Valeur    | Description                                               |
|----------|-----------------------------------------------------------|
| audio    | Musique et d’autres éléments audio uniquement                          |
| Autres    | D’autres éléments, tels qu’un fichier. ASF ou l’URL d’un flux. |
| photos    | Éléments de photo. requiert Lecteur Windows Media 10.            |
| playlist | Sélections représentées en tant qu’éléments multimédias.                     |
| radio    | Éléments de station de radio. non utilisé par Lecteur Windows Media 10. |
| video    | Éléments vidéo.                                              |



 

Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

pour plus d’informations sur les attributs pris en charge par Lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md).

Il existe deux façons de récupérer une interface **IWMPMediaCollection** , et le comportement de la méthode **getByAttribute** dépend de ceux de ces deux méthodes. Si vous récupérez l’interface en appelant [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), la méthode **getByAttribute** retourne tous les éléments multimédias de la bibliothèque. Toutefois, si vous récupérez l’interface en appelant [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), la méthode **getByAttribute** retourne uniquement les éléments audio de la bibliothèque qui ont l’attribut et la valeur spécifiés.

## <a name="examples"></a>Exemples

L’exemple de code suivant utilise **getByAttribute** pour lire tout le contenu de la bibliothèque par l’artiste nommé triode 48. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Get an interface to a playlist that contains media items by a particular artist.
WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
player.currentPlaylist = pl;

// Play the media items in the current playlist. 
player.Ctlcontrols.play();
```


```VB

' Get an interface to a playlist that contains media items by a particular artist.
Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAttribute(&quot;Artist&quot;, &quot;Triode 48&quot;)

&#39; Make the new playlist the current one.
player.currentPlaylist = pl

&#39; Play the media items in the current playlist. 
player.Ctlcontrols.play()
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
</dt> <dt>

[**IWMPPlaylistCollection. getAll (VB et C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)
</dt> </dl>

 

 





