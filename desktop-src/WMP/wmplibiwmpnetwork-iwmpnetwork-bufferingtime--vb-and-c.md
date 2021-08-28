---
title: IWMPNetwork propriété bufferingTime
description: La propriété bufferingTime obtient ou définit la durée en millisecondes allouée à la mise en mémoire tampon des données entrantes avant le début de la lecture.
ms.assetid: b5936b21-a17b-4801-a5fc-c6d6521e05aa
keywords:
- Lecteur Windows Media de la propriété bufferingTime
- Lecteur Windows Media de la propriété bufferingTime, interface IWMPNetwork
- Lecteur Windows Media de l’interface IWMPNetwork, propriété bufferingTime
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d224e35dd9c87dad627e71f2ae07d3d0b9e24ee1b094cfa5dea549e86c69a65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999989"
---
# <a name="iwmpnetworkbufferingtime-property"></a>IWMPNetwork :: bufferingTime, propriété

La propriété **bufferingTime** obtient ou définit la durée en millisecondes allouée à la mise en mémoire tampon des données entrantes avant le début de la lecture.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 bufferingTime {get; set;}
```


```VB

Public Property bufferingTime As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui correspond au temps de mise en mémoire tampon en millisecondes, qui est compris entre zéro et 60 000 avec une valeur par défaut de 5 000.

## <a name="examples"></a>Exemples

L’exemple de code suivant utilise **bufferingTime** pour spécifier le nombre de secondes allouées à la mise en mémoire tampon des données entrantes. Une zone de texte permet à l’utilisateur d’entrer une nouvelle valeur pour **bufferingTime**, et la propriété est mise à jour en réponse à l’événement de clic d’un bouton. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void setBufTime_Click(object sender, System.EventArgs e)
{
    // Retrieve input from the user and convert it to an integer.
    int newTime = System.Convert.ToInt32(bufText.Text);

    // Test whether the integer is within the valid range. 
    if (newTime >= 0 & newTime <= 60) 
    {
        // Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000);
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("Buffering time must be between 0 and 60.");
    }
}
```


```VB

Public Sub setBufTime_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setBufTime.Click

    &#39; Retrieve input from the user and convert it to an integer.
    Dim newTime As Integer = System.Convert.ToInt32(bufText.Text)

    &#39; Test whether the integer is within the valid range. 
    If (newTime >= 0 And newTime <= 60) Then

        &#39; Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000)

    Else

        System.Windows.Forms.MessageBox.Show(&quot;Buffering time must be between 0 and 60.&quot;)

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

[**Interface IWMPNetwork (VB et C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





