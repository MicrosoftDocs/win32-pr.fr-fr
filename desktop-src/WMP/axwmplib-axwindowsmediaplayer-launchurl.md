---
title: Méthode AxWindowsMediaPlayer. launchURL
description: La méthode launchURL envoie une URL au navigateur par défaut de l’utilisateur à restituer. | Méthode AxWindowsMediaPlayer. launchURL
ms.assetid: 3e8dfdbb-b5ad-44ea-97a6-e860386b7fb4
keywords:
- Lecteur Windows Media de la méthode launchURL
- méthode launchURL Lecteur Windows Media, classe AxWindowsMediaPlayer
- Lecteur Windows Media de la classe AxWindowsMediaPlayer, méthode launchURL
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.launchURL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27fe8e544bb14b119785b26b9cb5be5cdad48015
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856011"
---
# <a name="axwindowsmediaplayerlaunchurl-method"></a>Méthode AxWindowsMediaPlayer. launchURL

La méthode launchURL envoie une URL au navigateur par défaut de l’utilisateur à restituer.

## <a name="syntax"></a>Syntaxe


```CSharp
public void launchURL(
  System.String bstrURL
);
```


```VB

Public Sub launchURL( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrURL* 
</dt> <dd>

**System. String** qui correspond à l’URL à lancer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode ouvre uniquement les pages Web à l’aide des protocoles HTTP ou HTTPs.

## <a name="examples"></a>Exemples

L’exemple suivant crée un bouton qui, lorsque vous cliquez dessus, affiche le site Web Microsoft dans une nouvelle fenêtre de navigateur. L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.


```CSharp
private void goToMS_Click(object sender, System.EventArgs e)
{
    // Open the Microsoft website. 
    player.launchURL("https://www.microsoft.com");
}
```


```VB

Public Sub goToMS_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles goToMS.Click

    &#39; Open the Microsoft website. 
    player.launchURL(&quot;https://www.microsoft.com&quot;)

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

 

 





