---
title: Méthode IWMPMedia getMarkerName
description: La méthode getMarkerName retourne le nom du marqueur à l’index spécifié.
ms.assetid: 77f893cf-1669-41e3-9f62-8a1081e37add
keywords:
- Lecteur Windows Media de la méthode getMarkerName
- méthode getMarkerName Lecteur Windows Media, interface IWMPMedia
- Lecteur Windows Media de l’interface IWMPMedia, méthode getMarkerName
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ba6a7bb640a397cce9c7dfd22b5f9b6203c47
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228353"
---
# <a name="iwmpmediagetmarkername-method"></a>IWMPMedia :: getMarkerName, méthode

La méthode **getMarkerName** retourne le nom du marqueur à l’index spécifié.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String getMarkerName(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerName( _
  ByVal MarkerNum As System.Int32 _
) As System.String
Implements IWMPMedia.getMarkerName
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*MarkerNum* \[ dans\]
</dt> <dd>

**System. Int32** qui est l’index du marqueur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

**System. String** qui est le nom du marqueur.

## <a name="remarks"></a>Notes

Cette méthode retourne la **valeur null** si le marqueur spécifié n’existe pas.

Certains éléments multimédias ne contiennent pas de marqueurs. Utilisez **markerCount** pour déterminer le nombre de marqueurs qui se trouvent dans l’élément multimédia en cours.

Les numéros d’index des marqueurs commencent à 1.

Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

L’exemple de code suivant utilise **getMarkerName** pour remplir une zone de texte multiligne avec les noms des marqueurs dans l’élément multimédia en cours. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker names
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markers[i] = player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerNames.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mCount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker names
Dim markers(mCount) As String

&#39; Verify that at least one marker exists in the current media.
If (mCount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mCount

        &#39; Store the marker name in the array.
        markers(i) = player.currentMedia.getMarkerName(i)

    Next i

End If

&#39; Display the marker names in the text box.
markerNames.Lines = markers
```





## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. markerCount (VB et C#)**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





