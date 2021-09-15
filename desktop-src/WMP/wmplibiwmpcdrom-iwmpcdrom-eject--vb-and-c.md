---
title: Méthode EJECT IWMPCdrom
description: La méthode EJECT éjecte le CD ou DVD du lecteur. | Méthode EJECT IWMPCdrom
ms.assetid: c0a69252-fd79-452c-bc61-3c3e8bcaaf48
keywords:
- méthode eject Lecteur Windows Media
- eject, méthode Lecteur Windows Media, IWMPCdrom, interface
- Lecteur Windows Media de l’interface IWMPCdrom, méthode eject
topic_type:
- apiref
api_name:
- IWMPCdrom.eject
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ca2403b86b648e98861d91a21db80ddb64aac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530228"
---
# <a name="iwmpcdromeject-method"></a>IWMPCdrom :: EJECT, méthode

La méthode **EJECT** éjecte le CD ou DVD du lecteur.

## <a name="syntax"></a>Syntaxe


```CSharp
public void eject();
```


```VB

Public Sub eject()
Implements IWMPCdrom.eject
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si le loquet du lecteur est ouvert, cette méthode ferme la porte.

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

L’exemple suivant utilise **EJECT** pour ouvrir la porte du lecteur de CD ou de DVD dont l’index est égal à zéro en réponse à l’événement de clic d’un bouton. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void ejectButton_Click(object o, System.EventArgs args)
{
    player.cdromCollection.Item(0).eject();
}
```


```VB

Public Sub ejectButton_Click(ByVal o As Object, ByVal args As System.EventArgs) Handles ejectButton.Click

    player.cdromCollection.Item(0).eject()

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

[**AxWindowsMediaPlayer. lecture (VB et C#)**](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)
</dt> <dt>

[**Interface IWMPCdrom (VB et C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





