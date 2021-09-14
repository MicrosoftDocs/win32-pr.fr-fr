---
title: AxWindowsMediaPlayer. Close, méthode
description: la méthode close ferme le fichier multimédia numérique en cours, arrête la lecture dans Lecteur Windows Media et libère les ressources Lecteur Windows Media.
ms.assetid: 3e555086-c31c-42d7-b671-0fd824f66641
keywords:
- fermer la méthode Lecteur Windows Media
- close, méthode Lecteur Windows Media, AxWindowsMediaPlayer, classe
- Lecteur Windows Media de la classe AxWindowsMediaPlayer, méthode close
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.close
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc0c93e449e9ef1b00af7fb073068078f0fcc5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416264"
---
# <a name="axwindowsmediaplayerclose-method"></a>AxWindowsMediaPlayer. Close, méthode

la méthode close ferme le fichier multimédia numérique en cours, arrête la lecture dans Lecteur Windows Media et libère les ressources Lecteur Windows Media.

## <a name="syntax"></a>Syntaxe


```CSharp
public void close();
```


```VB

Public Sub close()
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

cette méthode ferme le fichier multimédia numérique en cours, et non Lecteur Windows Media lui-même.

## <a name="examples"></a>Exemples

l’exemple suivant crée un bouton qui, lorsque vous cliquez dessus, arrête la lecture dans Lecteur Windows Media et libère les ressources en cours d’utilisation. L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.


```CSharp
private void closeIt_Click(object sender, System.EventArgs e)
{
    // Close the Player. 
    player.close();
}
```


```VB

Public Sub closeIt_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles closeIt.Click

    &#39; Close the Player. 
    player.close()

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

 

 





