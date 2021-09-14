---
title: IWMPMediaCollection2 createQuery, méthode
description: La méthode createQuery retourne une interface IWMPQuery qui représente une nouvelle requête.
ms.assetid: a12da325-e77e-4e44-93d1-5e9c5733ea44
keywords:
- createQuery, méthode Lecteur Windows Media
- createQuery, méthode Lecteur Windows Media, IWMPMediaCollection2, interface
- interface IWMPMediaCollection2 Lecteur Windows Media, createQuery, méthode
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.createQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 318b27a20ba801e1fbed58ff79c5bed7841f8c29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292522"
---
# <a name="iwmpmediacollection2createquery-method"></a>IWMPMediaCollection2 :: createQuery, méthode

La `createQuery` méthode retourne une interface **IWMPQuery** qui représente une nouvelle requête.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPQuery createQuery();
```


```VB

Public Function createQuery() As IWMPQuery
Implements IWMPMediaCollection2.createQuery
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Interface **wmplib. IWMPQuery** qui représente une nouvelle requête vide.

## <a name="remarks"></a>Notes

La création d’une nouvelle requête est la première étape de la création d’une requête composée.

## <a name="examples"></a>Exemples

L’exemple suivant utilise `createQuery` pour récupérer une interface **IWMPQuery** qui est initialisée à la valeur null. Étant donné que cette requête n’a aucune condition ajoutée, quand elle est utilisée en tant qu’argument dans la méthode **getStringCollectionByQuery** , la méthode retourne une collection de chaînes qui contient tous les éléments multimédias du type de média spécifié. La collection de chaînes est ensuite affichée dans une zone de liste.


```CSharp
// Get an IWMPMediaCollection2 interface so that you can access the createQuery and
// getStringCollectionByQuery methods.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

// Create an IWMPQuery interface with no conditions added to it.
WMPLib.IWMPQuery nullQuery = mc.createQuery();

// Get a string collection that contains the titles of all the audio items in the media
// collection.
WMPLib.IWMPStringCollection2 allTitles = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", nullQuery, "audio", "", false);

// Display the titles by adding them to a list box.
for (int i = 0; i < allTitles.count; i++)
{
    queryResults.Items.Add(allTitles.Item(i));
}
```


```VB

' Get an IWMPMediaCollection2 interface so that you can access
&#39; the createQuery and getStringCollectionByQuery methods.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection

&#39; Create an IWMPQuery interface with no conditions added to it.
Dim nullQuery As WMPLib.IWMPQuery = mc.createQuery()

&#39; Get a string collection that contains the titles of all the audio items in the media
&#39; collection
Dim allTitles As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, nullQuery, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the titles by adding them to a ListBox
For i As Integer = 0 To (allTitles.count - 1)

    queryResults.Items.Add(allTitles.Item(i))

Next i
```





## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11.<br/>                                                                                    |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPMediaCollection2 (VB et C#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Interface IWMPQuery (VB et C#)**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





