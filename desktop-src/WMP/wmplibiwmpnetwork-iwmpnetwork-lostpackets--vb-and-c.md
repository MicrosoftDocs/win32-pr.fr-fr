---
title: IWMPNetwork propriété lostPackets
description: La propriété lostPackets obtient le nombre de paquets perdus.
ms.assetid: 611218d3-c4d3-4d4e-835c-1e7a956b2718
keywords:
- propriété lostPackets lecteur Windows Media
- propriété lostPackets lecteur Windows Media, interface IWMPNetwork
- Interface IWMPNetwork lecteur Windows Media, propriété lostPackets
topic_type:
- apiref
api_name:
- IWMPNetwork.lostPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1adac5f4aa8b1f58c023a556af04b8eae4bd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530992"
---
# <a name="iwmpnetworklostpackets-property"></a>IWMPNetwork :: lostPackets, propriété

La propriété **lostPackets** obtient le nombre de paquets perdus.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 lostPackets {get; set;}
```


```VB

Public ReadOnly Property lostPackets As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui correspond au nombre de paquets perdus.

## <a name="remarks"></a>Notes

Cette propriété comprend uniquement les paquets de diffusion multimédia en continu et retourne zéro lors de l’utilisation du protocole HTTP, qui est sans perte.

Les paquets peuvent être perdus pour plusieurs raisons, telles que le type et la qualité de la connexion réseau.

Chaque fois que la lecture est arrêtée et redémarrée, cette propriété est réinitialisée à zéro. La valeur n’est pas réinitialisée si la lecture est suspendue. Cette propriété obtient des informations valides uniquement au moment de l’exécution lorsque l’URL pour la lecture est définie à l’aide de la propriété **AxWindowsMediaPlayer. URL** .

## <a name="examples"></a>Exemples

L’exemple de code suivant utilise **lostPackets** pour afficher le nombre total de paquets perdus pendant la lecture. Les informations s’affichent dans une étiquette lorsque l’utilisateur clique sur un bouton. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void showLostPackets_Click(object sender, System.EventArgs e)
{
    lostPacketsLabel.Text = ("Packets lost: " + player.network.lostPackets.ToString());
}
```


```VB

Public Sub showLostPackets_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showLostPackets.Click

    lostPacketsLabel.Text = (&quot;Packets lost: &quot; + player.network.lostPackets.ToString())

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
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB et C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> </dl>

 

 





