---
title: IWMPControls propriété currentMarker
description: La propriété currentMarker obtient ou définit le numéro de marqueur actuel.
ms.assetid: faf8c32a-66de-47ce-aa3d-6699d9f9bdda
keywords:
- Lecteur Windows Media de la propriété currentMarker
- Lecteur Windows Media de la propriété currentMarker, interface IWMPControls
- Lecteur Windows Media de l’interface IWMPControls, propriété currentMarker
topic_type:
- apiref
api_name:
- IWMPControls.currentMarker
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfbcea42594b15b8da08248d38b5d8f72a1de29d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413308"
---
# <a name="iwmpcontrolscurrentmarker-property"></a>IWMPControls :: currentMarker, propriété

La propriété **currentMarker** obtient ou définit le numéro de marqueur actuel.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 currentMarker {get; set;}
```


```VB

Public Property currentMarker As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui est le numéro de marqueur.

## <a name="remarks"></a>Notes

La définition de **currentMarker** entraîne le démarrage de la lecture à partir du marqueur spécifié. Avant de tenter de définir **currentMarker**, déterminez si un fichier a des marqueurs et combien il a à l’aide de **IWMPMedia. markerCount**. Si un fichier n’a pas de marqueur, la définition de **currentMarker** sur n’importe quelle valeur, sauf zéro, génère une erreur. Si vous définissez **currentMarker** sur un nombre supérieur à **markerCount** , une erreur est également générée.

La propriété **currentMarker** retourne toujours le marqueur actuel ou le dernier marqueur, ce qui signifie que la position de fichier réelle peut être soit au marqueur actuel, soit avant le marqueur suivant. Les marqueurs sont numérotés à partir de 1. par conséquent, si un fichier a des marqueurs, vous pouvez affecter la valeur zéro à **currentMarker** pour changer la position du fichier.

Tant que l’élément multimédia actuel n’est pas défini (à l’aide de **AxWindowsMediaPlayer. URL** ou de **AxWindowsMediaPlayer. CurrentMedia**), **currentMarker** retourne zéro.

## <a name="examples"></a>Exemples

L’exemple suivant utilise **currentMarker** pour démarrer la lecture vidéo à partir du marqueur qui correspond à la propriété SelectedIndex d’une zone de liste qui a été remplie avec des identificateurs de marqueur. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Fill the list box with the marker identifiers of the current media item.
markers.Items.Add("Begining");
markers.Items.Add("Sunrise");
markers.Items.Add("Car chase");
markers.Items.Add("Happy ending");

// Set the currentMarker to the marker selected from the list box.
private void markers_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedMarker = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    player.Ctlcontrols.currentMarker = selectedMarker;
}
```


```VB

' Fill the list box with the marker identifiers of the current media item.
markers.Items.Add(&quot;Begining&quot;)
markers.Items.Add(&quot;Sunrise&quot;)
markers.Items.Add(&quot;Car chase&quot;)
markers.Items.Add(&quot;Happy ending&quot;)

&#39; Set the currentMarker to the marker selected from the list box.
Public Sub markers_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles markers.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedMarker As Integer = lb.SelectedIndex

    player.Ctlcontrols.currentMarker = selectedMarker

End Sub
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

[**AxWindowsMediaPlayer. URL (VB et C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interface IWMPControls (VB et C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. markerCount (VB et C#)**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





