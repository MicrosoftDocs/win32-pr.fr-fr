---
title: AxWindowsMediaPlayer. fullScreen, propriété
description: La propriété fullScreen obtient ou définit une valeur indiquant si le contenu vidéo est lu en mode plein écran.
ms.assetid: 6c48a54a-e0f1-4bf5-8a53-7ccc78fc76ad
keywords:
- Lecteur Windows Media de propriété fullScreen
- propriété fullScreen Lecteur Windows Media, classe AxWindowsMediaPlayer
- Lecteur Windows Media de la classe AxWindowsMediaPlayer, propriété fullScreen
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.fullScreen
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23bfb1a2c67ecfa3ba7cced6f0ccb564bb387b52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192424"
---
# <a name="axwindowsmediaplayerfullscreen-property"></a>AxWindowsMediaPlayer. fullScreen, propriété

La propriété fullScreen obtient ou définit une valeur indiquant si le contenu vidéo est lu en mode plein écran.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Boolean fullScreen {get; set;}
```


```VB

Public Property fullScreen As System.Boolean
```





## <a name="property-value"></a>Valeur de la propriété

Valeur System. Boolean qui indique si le contenu est lu en mode plein écran. La valeur par défaut est false.

## <a name="remarks"></a>Notes

pour que le mode plein écran fonctionne correctement lors de l’incorporation du contrôle Lecteur Windows Media, la zone d’affichage vidéo doit avoir une hauteur et une largeur d’au moins un pixel. Si **UIMODE** a la valeur « mini » ou « Full », la hauteur du contrôle lui-même doit être supérieure ou égale à 65 pour s’adapter à la zone d’affichage vidéo en plus de l’interface utilisateur.

Si **UIMODE** a la valeur « invisible », l’affectation de la valeur true à cette propriété génère une erreur et n’affecte pas le comportement du contrôle.

pendant la lecture en plein écran, Lecteur Windows Media masque le curseur de la souris quand [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) est égal à false et **uiMode** est égal à « none ».

si **uiMode** a la valeur « full » ou « mini », Lecteur Windows Media affiche les contrôles de transport en mode plein écran lorsque le curseur de la souris se déplace. Après un bref intervalle d’absence de mouvement de la souris, les contrôles de transport sont masqués. Si **UIMODE** a la valeur « None », aucun contrôle n’est affiché en mode plein écran.

> [!Note]  
> l’affichage des contrôles de transport en mode plein écran nécessite le système d’exploitation Windows XP.

 

si les contrôles de transport ne s’affichent pas en mode plein écran, Lecteur Windows Media quitte automatiquement le mode plein écran lorsque la lecture s’arrête.

## <a name="examples"></a>Exemples

L’exemple suivant crée un bouton qui utilise la propriété fullScreen pour faire basculer un objet lecteur incorporé en mode plein écran. L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.


```CSharp
private void fullScreen_Click(object sender, System.EventArgs e)
{
    // If the player is playing, switch to full screen. 
    if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
    {
        player.fullScreen = true;
    }
}
```


```VB

Public Sub fullScreen_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fullScreen.Click

    &#39; If the player is playing, switch to full screen. 
    If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

        player.fullScreen = True

    End If

End Sub
```





## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|--------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                  |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                            |
| Assembly<br/>  | <dl> <dt>AxInterop. WMPLib (AxInterop.WMPLib.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. uiMode (VB et C#)**](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)
</dt> </dl>

 

 





