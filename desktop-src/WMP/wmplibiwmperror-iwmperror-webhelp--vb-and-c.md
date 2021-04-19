---
title: IWMPError Webhelp, méthode
description: La méthode Webhelp ouvre la page d’aide Web du lecteur Windows Media pour afficher des informations supplémentaires sur la première erreur de la file d’attente des erreurs (index zéro). | IWMPError Webhelp, méthode
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- méthode Webhelp lecteur Windows Media
- méthode Webhelp lecteur Windows Media, interface IWMPError
- Interface IWMPError Windows Media Player, Webhelp, méthode
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
ms.openlocfilehash: 6c9b0cd48d45ac5e5e5d77d0150b8acdf13347e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533449"
---
# <a name="iwmperrorwebhelp-method"></a>IWMPError :: Webhelp, méthode

La méthode **Webhelp** ouvre la page d’aide Web du lecteur Windows Media pour afficher des informations supplémentaires sur la première erreur de la file d’attente des erreurs (index zéro).

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

## <a name="remarks"></a>Notes

Les pages d’aide Web contiennent toujours les informations les plus récentes et les plus détaillées sur les erreurs du lecteur Windows Media. Cette méthode transfère automatiquement les autres informations requises par l’aide Web, telles que la version du système d’exploitation utilisée.

Pour accéder directement aux pages d’aide Web, utilisez le code d’erreur suivant et les liens du centre d’aide et de support :

-   [Informations de code d’erreur du lecteur Windows Media](https://support.microsoft.com/kb/886273)
-   [Centre de solutions du lecteur Windows Media](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a>Exemples

L’exemple suivant crée un bouton qui lance la page d’aide Web du lecteur Microsoft Windows Media dans le navigateur. L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.


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

 

 





