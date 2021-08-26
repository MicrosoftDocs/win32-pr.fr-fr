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
ms.openlocfilehash: 3b4f3ad10a6defe4e7db252a1703888550ff5a89fe2a0d0618dd9886fc5f74bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123989"
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

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

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





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





