---
title: IWMPControls currentItem, propriété
description: La propriété currentItem obtient ou définit l’élément multimédia actuel dans une sélection.
ms.assetid: 0a331b1f-95bd-48ea-b951-1ca35cc96865
keywords:
- currentItem, propriété Lecteur Windows Media
- currentItem, Lecteur Windows Media de propriété, interface IWMPControls
- Lecteur Windows Media de l’interface IWMPControls, propriété currentItem
topic_type:
- apiref
api_name:
- IWMPControls.currentItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae04eb333e2fd347fa6f88b33ec2482a4dd8fd7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413309"
---
# <a name="iwmpcontrolscurrentitem-property"></a>IWMPControls :: currentItem, propriété

La propriété **CurrentItem** obtient ou définit l’élément multimédia actuel dans une sélection.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPMedia currentItem {get; set;}
```


```VB

Public Property currentItem As IWMPMedia
```





## <a name="property-value"></a>Valeur de la propriété

Interface **wmplib. IWMPMedia** qui représente l’élément multimédia.

## <a name="remarks"></a>Notes

Cette propriété fonctionne uniquement avec les éléments de la sélection actuelle. La définition de **CurrentItem** sur l’interface d’un élément multimédia enregistré n’est pas prise en charge.

## <a name="examples"></a>Exemples

L’exemple suivant utilise **CurrentItem** pour définir l’élément multimédia actuel du joueur sur un élément sélectionné dans une zone de liste. La zone de liste a été remplie avec tous les éléments de la sélection actuelle. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void playItem_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedItem = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop();

    // Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.get_Item(selectedItem);
    
    // Play the current item.
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playItem_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles playItem.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedItem As Integer = lb.SelectedIndex

    &#39; Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop()

    &#39; Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.Item(selectedItem)

    &#39; Play the current item.
    player.Ctlcontrols.play()

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

[**IWMPControlsInterface (VB et C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPMediaInterface (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getByName (VB et C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





