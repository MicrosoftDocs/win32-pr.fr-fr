---
title: IWMPError Webhelp, méthode
description: la méthode webhelp lance la Lecteur Windows Media page d’aide Web pour afficher des informations supplémentaires sur la première erreur de la file d’attente des erreurs (index zéro). | IWMPError Webhelp, méthode
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- Lecteur Windows Media de la méthode webhelp
- Lecteur Windows Media de la méthode webhelp, interface IWMPError
- Lecteur Windows Media de l’interface IWMPError, webhelp, méthode
topic_type:
- apiref
api_name:
- IWMPError.webHelp
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50d4b404988e8b317ec7b090adcb96aac8e26a5a82590aa1138848dc797e3e79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115822"
---
# <a name="iwmperrorwebhelp-method"></a>IWMPError :: Webhelp, méthode

la méthode **webhelp** lance la Lecteur Windows Media page d’aide Web pour afficher des informations supplémentaires sur la première erreur de la file d’attente des erreurs (index zéro).

## <a name="syntax"></a>Syntaxe


```CSharp
public void webHelp();
```


```VB

Public Sub webHelp()
Implements IWMPError.webHelp
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

les pages d’aide Web contiennent toujours les informations les plus récentes et les plus détaillées sur les erreurs de Lecteur Windows Media. Cette méthode transfère automatiquement les autres informations requises par l’aide Web, telles que la version du système d’exploitation utilisée.

Pour accéder directement aux pages d’aide Web, utilisez le code d’erreur suivant et les liens du centre d’aide et de support :

-   [Lecteur Windows Media Informations sur le code d’erreur](https://support.microsoft.com/kb/886273)
-   [Lecteur Windows Media Centre de solutions](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a>Exemples

l’exemple suivant crée un bouton qui lance la page d’aide Web de Microsoft Lecteur Windows Media dans le navigateur. L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.


```CSharp
private void webHelpButton_Click(object sender, System.EventArgs e)
{
    // Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp();
}
```


```VB

Public Sub webHelpButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles webHelpButton.Click

    &#39; Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp()

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

[**Interface IWMPError (VB et C#)**](iwmperror--vb-and-c.md)
</dt> </dl>

 

 





