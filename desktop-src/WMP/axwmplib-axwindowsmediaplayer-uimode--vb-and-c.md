---
title: AxWindowsMediaPlayer. uiMode, propriété
description: La propriété uiMode obtient ou définit une valeur indiquant les contrôles qui sont affichés dans l’interface utilisateur.
ms.assetid: 01034418-be70-44f3-8812-e529c747c9e4
keywords:
- propriété uiMode lecteur Windows Media
- propriété uiMode lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété uiMode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.uiMode
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33edcf6bdff9e1587269df9eb49c3729099d091e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528930"
---
# <a name="axwindowsmediaplayeruimode-property"></a>AxWindowsMediaPlayer. uiMode, propriété

La propriété uiMode obtient ou définit une valeur indiquant les contrôles qui sont affichés dans l’interface utilisateur.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String uiMode {get; set;}
```


```VB

Public Property uiMode As System.String
```





## <a name="property-value"></a>Valeur de la propriété

System. String qui est l’une des valeurs suivantes.



| Valeur     | Description                                                                                                                                                                                                     | Exemple audio                                                   | Exemple de vidéo                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------|
| invisibles | Le lecteur Windows Media est incorporé sans aucune interface utilisateur visible (fenêtre contrôles, vidéo ou visualisation).                                                                                                  | (Rien ne s’affiche.)                                         | (Rien ne s’affiche.)                                         |
| aucun      | Le lecteur Windows Media est incorporé sans contrôles, et seule la fenêtre vidéo ou visualisation s’affiche.                                                                                                   | ![UIMODE = 'none’avec l’audio](images/uimode-none-audio-v11.png) | ![UIMODE = 'none’avec vidéo](images/uimode-none-video-v11.png) |
| minimales      | Le lecteur Windows Media est incorporé avec la fenêtre d’État, les commandes lecture/pause, arrêter, muet et volume affichées en plus de la fenêtre vidéo ou visualisation.                                                    | ![UIMODE = 'mini’avec l’audio](images/uimode-mini-audio-v11.png) | ![UIMODE = 'mini’avec vidéo](images/uimode-mini-video-v11.png) |
| complet      | Par défaut. Le lecteur Windows Media est intégré à la fenêtre d’État, à la barre de recherche, aux commandes lecture/pause, arrêter, muet, suivant, précédent, avance rapide, rembobiner et volume, en plus de la fenêtre vidéo ou visualisation. | ![UIMODE = 'Full’avec l’audio](images/uimode-full-audio-v11.png) | ![UIMODE = 'Full’avec vidéo](images/uimode-full-video-v11.png) |
| custom    | Le lecteur Windows Media est incorporé avec une interface utilisateur personnalisée. Ne peut être utilisé que dans les programmes C++.                                                                                                                | (L’interface utilisateur personnalisée s’affiche.)                           | (L’interface utilisateur personnalisée s’affiche.)                           |



 

## <a name="remarks&quot;></a>Notes

Cette propriété spécifie l’apparence du lecteur Windows Media incorporé. Lorsque **UIMODE** a la valeur « None », « mini » ou « Full », une fenêtre est présente pour l’affichage des clips vidéo et des visualisations audio. Cette fenêtre peut être masquée en mode mini ou en mode complet en affectant à l’attribut **Height** de la balise **OBJECT** la valeur 40, qui est mesurée à partir du bas et laisse la partie Controls de l’interface utilisateur visible. Si aucune interface incorporée n’est souhaitée, affectez la valeur zéro aux attributs **Width** et **Height** .

Si **UIMODE** est défini sur « invisible », aucune interface utilisateur n’est affichée, mais l’espace est toujours réservé sur la page, comme indiqué par **Width** et **Height**. Cela est utile pour conserver la mise en page quand **UIMODE** peut changer. En outre, l’espace réservé est transparent, de sorte que tous les éléments superposés derrière le contrôle sont visibles.

Si **UIMODE** a la valeur « Full » ou « mini », le lecteur Windows Media affiche les contrôles de transport en mode plein écran. Si **UIMODE** a la valeur « None », aucun contrôle n’est affiché en mode plein écran.

Si la fenêtre est visible et que le contenu audio est lu, la visualisation affichée sera celle qui est la plus récemment utilisée dans le lecteur Windows Media.

Si **UIMODE** a la valeur « Custom » dans un programme C++ qui implémente **IWMPRemoteMediaServices**, le fichier d’apparence indiqué par **IWMPRemoteMediaServices. GetCustomUIMode** s’affiche.

Pendant la lecture en plein écran, le lecteur Windows Media masque le curseur de la souris quand **enableContextMenu** est égal à false et **UIMODE** est égal à « None ».

## <a name=&quot;examples&quot;></a>Exemples

L’exemple suivant crée une zone de liste qui permet à l’utilisateur de modifier le mode d’interface utilisateur d’un objet lecteur Windows Media incorporé. L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.


```CSharp
// Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible");
uiModeOptions.Items.Add("none");
uiModeOptions.Items.Add("mini");
uiModeOptions.Items.Add("full");


private void uiModeOptions_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Get the selected UI mode in the list box as a string.
    string newMode = (string)(((System.Windows.Forms.ListBox)sender).SelectedItem);
     
    // Set the UI mode that the user selected.
    player.uiMode = newMode;            
}
```


```VB

' Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible&quot;)
uiModeOptions.Items.Add(&quot;none&quot;)
uiModeOptions.Items.Add(&quot;mini&quot;)
uiModeOptions.Items.Add(&quot;full&quot;)


Public Sub uiModeOptions_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles uiModeOptions.SelectedIndexChanged

    &#39; Get the selected UI mode in the list box as a string.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim newMode As String = lb.SelectedItem

    &#39; Set the UI mode that the user selected.
    player.uiMode = newMode

End Sub
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media version 7,0 ou ultérieure. Lecteur Windows Media série 9 ou version ultérieure pour « invisible » ou « personnalisé »<br/>   |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. enableContextMenu (VB et C#)**](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)
</dt> </dl>

 

 





