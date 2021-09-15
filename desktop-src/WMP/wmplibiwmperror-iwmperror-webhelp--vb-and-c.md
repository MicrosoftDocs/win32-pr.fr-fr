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
ms.openlocfilehash: 6c9b0cd48d45ac5e5e5d77d0150b8acdf13347e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403697"
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

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

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





## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPError (VB et C#)**](iwmperror--vb-and-c.md)
</dt> </dl>

 

 





