---
title: AxWindowsMediaPlayer. URL (propriété)
description: La propriété URL obtient ou définit le nom de l’élément multimédia à lire.
ms.assetid: 521a3b39-efd6-45a7-895b-a9ae69e0bf39
keywords:
- Lecteur Windows Media de propriété URL
- Lecteur Windows Media de propriété URL, classe AxWindowsMediaPlayer
- Lecteur Windows Media de la classe AxWindowsMediaPlayer, propriété URL
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.URL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ed9e601aa581e988bac1a233f06c4f5c552353
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193303"
---
# <a name="axwindowsmediaplayerurl-property"></a>AxWindowsMediaPlayer. URL (propriété)

La propriété URL obtient ou définit le nom de l’élément multimédia à lire.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String URL {get; set;}
```


```VB

Public Property URL As System.String
```





## <a name="property-value"></a>Valeur de la propriété

System. String qui est l’URL de l’élément multimédia.

## <a name="remarks"></a>Notes

Cette propriété peut uniquement être définie sur une URL dans une zone de sécurité identique ou moins restrictive que la zone de sécurité du programme ou de la page Web appelante.

Les applications qui ouvrent des éléments multimédias à partir d’un pare-feu offrent de meilleures performances si l’adresse est spécifiée à l’aide du nom DNS (Domain Name Server) au lieu de l’adresse IP.

N’appelez pas cette méthode à partir du code du gestionnaire d’événements. L’appel de l' **URL** à partir d’un gestionnaire d’événements peut donner des résultats inattendus.

## <a name="examples"></a>Exemples

L’exemple suivant permet à l’utilisateur de spécifier un fichier multimédia en entrant un chemin d’accès de fichier dans une zone de texte. Lorsqu’un utilisateur clique sur un bouton, la propriété URL est définie sur le fichier spécifié et le fichier est lu. L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.


```CSharp
private void openMedia_Click(object sender, System.EventArgs e)
{
    // Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text;

    // Play the media file. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub openMedia_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles openMedia.Click

    &#39; Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text

    &#39; Play the media file. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





