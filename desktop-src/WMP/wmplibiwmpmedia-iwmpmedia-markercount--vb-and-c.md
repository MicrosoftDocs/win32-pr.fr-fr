---
title: IWMPMedia propriété markerCount
description: La propriété markerCount obtient le nombre de marqueurs dans l’élément multimédia.
ms.assetid: d1ccaa9b-98fb-4c53-8064-ee4bf718d18a
keywords:
- Lecteur Windows Media de la propriété markerCount
- Lecteur Windows Media de la propriété markerCount, interface IWMPMedia
- Lecteur Windows Media de l’interface IWMPMedia, propriété markerCount
topic_type:
- apiref
api_name:
- IWMPMedia.markerCount
- IWMPMedia.get_markerCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdad591d8be66dcd20bc5e59d206a637d9b1181f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416151"
---
# <a name="iwmpmediamarkercount-property"></a>IWMPMedia :: markerCount, propriété

La propriété **markerCount** obtient le nombre de marqueurs dans l’élément multimédia.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 markerCount {get;}
```


```VB

Public ReadOnly Property markerCount As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui est le nombre de marqueurs.

## <a name="remarks"></a>Notes

Cette propriété retourne la valeur zéro si un fichier n’a pas de marqueurs, ou si l’élément multimédia n’est pas le même que celui spécifié dans AxWindowsMediaPlayer. currentMedia.

Les numéros des marqueurs commencent à 1.

Avant d’utiliser cette propriété, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

L’exemple suivant utilise **markerCount** pour récupérer le nombre de marqueurs dans l’élément multimédia en cours. Cette valeur est ensuite utilisée comme limite supérieure pour une structure de bouclage, qui itère au sein de la liste de marqueurs pour récupérer chaque nom de marqueur et l’affiche dans une zone de texte multiligne. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of markers.
string[] markerNames = new string[mcount];

// Verify that at least one marker exists in the current media item.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markerNames[i]= player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerList.Lines = markerNames;            
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of markers.
Dim markerNames(mcount) As String

&#39; Verify that at least one marker exists in the current media item.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker name in the array.
        markerNames(i) = player.currentMedia.getMarkerName(i)

    Next i

    &#39; Display the marker names in the text box.
    markerList.Lines = markerNames

End If
```





## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AxWindowsMediaPlayer. currentMedia (VB et C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





