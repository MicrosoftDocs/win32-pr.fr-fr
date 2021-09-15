---
title: Propriété Duration de IWMPMedia
description: La propriété Duration obtient la durée en secondes de l’élément multimédia actuel.
ms.assetid: f8a0bf3e-eeaf-46f5-90c8-d3b11ce4eb39
keywords:
- propriété duration Lecteur Windows Media
- propriété duration Lecteur Windows Media, interface IWMPMedia
- Lecteur Windows Media de l’interface IWMPMedia, propriété duration
topic_type:
- apiref
api_name:
- IWMPMedia.duration
- IWMPMedia.get_duration
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f796cab042713082ce2066659f62736855e62787
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413304"
---
# <a name="iwmpmediaduration-property"></a>IWMPMedia ::d propriété figuration

La propriété **Duration** obtient la durée en secondes de l’élément multimédia actuel.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Double duration {get;}
```


```VB

Public ReadOnly Property duration As System.Double
```





## <a name="property-value"></a>Valeur de la propriété

**System. double** qui correspond à la durée en secondes.

## <a name="remarks"></a>Notes

Si cette propriété est utilisée avec un élément multimédia autre que celui spécifié dans AxWindowsMediaPlayer. currentMedia, elle ne peut pas contenir de valeur valide.

pour récupérer la durée des fichiers qui ne sont pas dans la bibliothèque de l’utilisateur, vous devez attendre que Lecteur Windows Media ouvre le fichier ; autrement dit, le **OpenState** actuel doit être égal à **MediaOpen**. Vous pouvez le vérifier en gérant **AxWindowsMediaPlayer. \_ Événement WMPOCXEvents \_ OpenStateChange** ou en vérifiant régulièrement la valeur de **AxWindowsMediaPlayer. openState**.

Pour les sélections, la durée de chaque élément multimédia peut être récupérée lors de l’ouverture de l’élément multimédia individuel, plutôt que lors de l’ouverture de la sélection.

Avant d’utiliser cette propriété, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

L’exemple suivant utilise **Duration** pour afficher l’heure restante dans l’élément multimédia actuel dans une étiquette. Un minuteur met à jour le texte de l’étiquette chaque seconde.


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 

private void TimerEventProcessor(object sender, System.EventArgs e)
{
    // Subtract the current position from the duration of the current media to get
    // the time remaining. Use the Math.floor method to round the result down to the
    // nearest whole number.
    double t = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition);

    // Display the time remaining in the current media.
    timeRemaining.Text = ("Seconds remaining: " + t.ToString());        
}
```


```VB

' Set the timer to fire an event every second and start the timer.
Timer.Interval = 1000
Timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a Select Case statement to
&#39; determine when to start and stop the timer. 

Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles Timer.Tick

    &#39; Subtract the current position from the duration of the current media to get
    &#39; the time remaining. Use the Math.Floor method to round the result down to the
    &#39; nearest whole number.
    Dim t As Double = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition)

    &#39; Display the time remaining in the current media.
    timeRemaining.Text = (&quot;Seconds remaining: &quot; + t.ToString())

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

[**AxWindowsMediaPlayer. openState (VB et C#)**](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> <dt>

[**événement AxWindowsMediaPlayer. OpenStateChange (VB et C#)**](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. durationString (VB et C#)**](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)
</dt> </dl>

 

 





