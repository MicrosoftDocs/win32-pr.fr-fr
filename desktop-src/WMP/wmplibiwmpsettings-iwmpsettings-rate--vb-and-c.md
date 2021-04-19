---
title: Propriété de la fréquence IWMPSettings
description: La propriété rate obtient ou définit la vitesse de lecture actuelle pour la vidéo.
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- propriété rate Windows Media Player
- propriété rate lecteur Windows Media, interface IWMPSettings
- Interface IWMPSettings lecteur Windows Media, propriété rate
topic_type:
- apiref
api_name:
- IWMPSettings.rate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f502bebdbd22523858637f8abccbe203db104cbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523523"
---
# <a name="iwmpsettingsrate-property"></a>IWMPSettings :: rate, propriété

La propriété **rate** obtient ou définit la vitesse de lecture actuelle pour la vidéo.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a>Valeur de la propriété

**System. double** qui est la vitesse de lecture, avec une valeur par défaut de 1,0.

## <a name="remarks"></a>Notes

La valeur récupérée par cette propriété agit comme une valeur de multiplicateur qui vous permet de lire un élément multimédia à un débit plus rapide ou plus lent. La valeur par défaut 1,0 indique la vitesse créée.

Notez qu’une piste audio devient difficile à comprendre à des vitesses inférieures à 0,5 ou supérieures à 1,5. Un taux de lecture de 2 indique deux fois la vitesse de lecture normale.

Le lecteur Windows Media tentera d’utiliser le plus efficace des quatre modes de lecture suivants

-   Lecture vidéo lissée avec maintien de la tonalité audio
-   Lecture vidéo lisse avec la tonalité audio non gérée
-   Lecture vidéo lissée sans audio
-   Lecture vidéo de l’image clé sans audio

Le mode choisi par le lecteur Windows Media dépend de nombreux facteurs, notamment le type de fichier et l’emplacement, le système d’exploitation, le réseau et le serveur.

D’autres considérations s’appliquent également, en fonction du format de média numérique utilisé pour créer le contenu :

-   **Windows Media Video (WMV) et ASF.** Les valeurs optimales pour la propriété **rate** sont comprises entre 1 et 10, ou entre 1 et 10 pour la lecture inversée. Les valeurs comprises entre 0,5 et 1,0 ou de-0,5 à-1,0 peuvent également fonctionner correctement dans les cas où la tonalité audio peut être conservée, par exemple lors de la lecture de fichiers situés sur l’ordinateur local. Les valeurs avec une magnitude absolue supérieure à 10 sont autorisées, mais elles ne sont pas très explicites.
-   **Autres formats vidéo.** La propriété **rate** peut être comprise entre 0 et 9. Les valeurs négatives ne sont pas autorisées. Les valeurs inférieures à 1 représentent un mouvement lent. Les valeurs supérieures à 9 sont autorisées, mais elles ne sont pas très explicites.

La méthode **IWMPControls. fastForward** remplace la valeur de **rate** par 5,0, tandis que la méthode **IWMPControls. fastReverse** change la valeur de **rate** en 5,0.

La vitesse de lecture de certains formats multimédias numériques ne peut pas être modifiée. Utilisez la propriété **IWMPSettings. isAvailable** (en C#, la méthode **IWMPSettings. obtenir \_ isAvailable** ) pour déterminer si cette propriété peut être spécifiée pour un élément multimédia particulier.

## <a name="examples"></a>Exemples

L’exemple suivant utilise un contrôle de type UpDown numérique qui permet à l’utilisateur de modifier la vitesse de lecture du média actuel. Quand l’utilisateur clique sur les flèches haut ou bas du contrôle, la propriété **rate** est définie sur la nouvelle valeur. La plage de valeurs possible dans le contrôle est 0,5 (demi-vitesse) à 2,0 (double vitesse). L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void playbackRate_Click(object sender, System.EventArgs e)
{
    // Get the new value of the control, and cast it from decimal to double.
    double newRate = (double)((System.Windows.Forms.NumericUpDown)sender).Value;

    // Test whether playback rate can be set. 
    if( player.settings.get_isAvailable("Rate") )
    {
        // Set the playback rate to the new value.
        player.settings.rate = newRate;
    }
}
```


```VB

Public Sub playbackRate_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playbackRate.Click

    &#39;  Get the new value of the control as a double.
    Dim nUpDown As System.Windows.Forms.NumericUpDown = sender
    Dim newRate As Double = nUpDown.Value

    &#39;  Test whether playback rate can be set. 
    If (player.settings.isAvailable(&quot;Rate&quot;)) Then

        &#39;  Set the playback rate to the new value.
        player.settings.rate = newRate

    End If

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

[**IWMPControls. fastForward (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**IWMPControls. fastReverse (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[**Interface IWMPSettings (VB et C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. isAvailable (VB et C#)**](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. MUTE (VB et C#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 





