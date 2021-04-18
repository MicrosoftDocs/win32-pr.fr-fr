---
title: Méthode IWMPCdromCollection getByDriveSpecifier
description: La méthode getByDriveSpecifier retourne une interface IWMPCdrom associée à une lettre de lecteur particulière.
ms.assetid: 4a550eb1-a37e-43fd-9e08-801c4fd64e68
keywords:
- méthode getByDriveSpecifier lecteur Windows Media
- méthode getByDriveSpecifier lecteur Windows Media, interface IWMPCdromCollection
- Interface IWMPCdromCollection lecteur Windows Media, méthode getByDriveSpecifier
topic_type:
- apiref
api_name:
- IWMPCdromCollection.getByDriveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe771fc893d4bf43b82dc825a2d33724926e8151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543211"
---
# <a name="iwmpcdromcollectiongetbydrivespecifier-method"></a>IWMPCdromCollection :: getByDriveSpecifier, méthode

La méthode **getByDriveSpecifier** retourne une interface **IWMPCdrom** associée à une lettre de lecteur particulière.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPCdrom getByDriveSpecifier(
  System.String bstrDriveSpecifier
);
```


```VB

Public Function getByDriveSpecifier( _
  ByVal bstrDriveSpecifier As System.String _
) As IWMPCdrom
Implements IWMPCdromCollection.getByDriveSpecifier
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrDriveSpecifier* \[ dans\]
</dt> <dd>

**System. String** qui est la lettre de lecteur suivie d’un signe deux-points («  : »).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Interface **wmplib. IWMPCdrom** .

## <a name="remarks"></a>Notes

Les lettres de lecteur doivent être indiquées sous la forme *x*:, où *x* représente la lettre de lecteur.

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="examples"></a>Exemples

L’exemple suivant utilise **getByDriveSpecifier** pour obtenir l’interface **IWMPCdrom** qui correspond à une lettre de lecteur fournie par l’utilisateur dans une zone de texte. La méthode **IWMPCdrom. EJECT** est ensuite appelée pour éjecter le lecteur spécifié. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Store the drive letter provided by the user.
string driveLetter = myText.Text;

// Append a colon to the drive letter to create a valid drive specifier.
driveLetter += ":";

// Get an IWMPCdrom interface for the drive.
WMPLib.IWMPCdrom drive = player.cdromCollection.getByDriveSpecifier(driveLetter);

// Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject();
```


```VB

' Store the drive letter provided by the user.
Dim driveLetter As String = myText.Text

&#39; Append a colon to the drive letter to create a valid drive specifier.
driveLetter += &quot;:&quot;

&#39; Get an IWMPCdrom interface for the drive.
Dim drive As WMPLib.IWMPCdrom = player.cdromCollection.getByDriveSpecifier(driveLetter)

&#39; Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject()
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPCdrom (VB et C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPCdrom. EJECT (VB et C#)**](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md)
</dt> <dt>

[**Interface IWMPCdromCollection (VB et C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





