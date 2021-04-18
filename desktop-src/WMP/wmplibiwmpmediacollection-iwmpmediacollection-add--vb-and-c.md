---
title: IWMPMediaCollection Add (méthode)
description: La méthode Add ajoute un nouvel élément multimédia ou une nouvelle sélection à la bibliothèque. | IWMPMediaCollection Add (méthode)
ms.assetid: a3539646-797b-4481-a31e-86771f3633a9
keywords:
- Ajouter une méthode lecteur Windows Media
- Add, méthode lecteur Windows Media, interface IWMPMediaCollection
- Interface IWMPMediaCollection lecteur Windows Media, méthode Add
topic_type:
- apiref
api_name:
- IWMPMediaCollection.add
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7953067281e394df71a1a53c874cb80837a5f35d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532713"
---
# <a name="iwmpmediacollectionadd-method"></a>IWMPMediaCollection :: Add, méthode

La méthode **Add** ajoute un nouvel élément multimédia ou une nouvelle sélection à la bibliothèque.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPMedia add(
  System.String bstrURL
);
```


```VB

Public Function add( _
  ByVal bstrURL As System.String _
) As IWMPMedia
Implements IWMPMediaCollection.add
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*du bstrURL* \[ dans\]
</dt> <dd>

**System. String** qui est l’URL qui spécifie l’emplacement de l’élément multimédia ou de la sélection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Interface **wmplib. IWMPMedia** pour l’élément ajouté ou la sélection.

## <a name="remarks"></a>Notes

Cette méthode charge un élément multimédia existant ou une sélection dans la bibliothèque, en fonction d’un chemin d’accès. Cette méthode ne déplace pas ou ne modifie pas le fichier. Cette méthode échoue si le chemin d’accès local n’est pas valide, mais que la validité des éléments de média n’est pas vérifiée avant leur ajout à la bibliothèque.

Cette méthode accepte à la fois les fichiers de sélection statique et automatique. La méthode **IWMPPlaylistCollection. importPlaylist** peut également être utilisée pour ajouter une sélection statique à la bibliothèque.

Avant d’appeler cette méthode, vous devez disposer d’un accès complet à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

L’exemple suivant ajoute trois objets multimédias à la collection de supports du lecteur Windows Media. L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.


```CSharp
// Adding a media object using a website.
player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"\\yourservername\Public\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"C:\WMSDK\WMPSDK\samples\media\house.wma");
```


```VB

' Adding a media object using a website.
player.mediaCollection.add(&quot;http:&#39;www.proseware.com/Media/Laure.wma&quot;)

&#39; Adding a media object from a local network.
player.mediaCollection.add(&quot;\\yourservername\Public\Jeanne.wma&quot;)

&#39; Adding a media object from a file on a local drive.
player.mediaCollection.add(&quot;C:\WMSDK\WMPSDK\samples\media\house.wma&quot;)
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

[**IWMPMediaCollection. Remove (VB et C#)**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. importPlaylist (VB et C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> </dl>

 

 





