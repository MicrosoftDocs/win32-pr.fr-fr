---
title: Méthode CdromCollection. getByDriveSpecifier
description: La méthode getByDriveSpecifier récupère l’objet cdrom associé à une lettre de lecteur particulière.
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- Lecteur Windows Media de la méthode getByDriveSpecifier
- méthode getByDriveSpecifier Lecteur Windows Media, classe CdromCollection
- Lecteur Windows Media de la classe CdromCollection, méthode getByDriveSpecifier
topic_type:
- apiref
api_name:
- CdromCollection.getByDriveSpecifier
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa5487b3a57fb1e7e4167561fcca08e10d6472182881fa221bd8e671bc814cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864089"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a>Méthode CdromCollection. getByDriveSpecifier

La méthode **getByDriveSpecifier** récupère l’objet **cdrom** associé à une lettre de lecteur particulière.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*driveSpecifier* \[ dans\]
</dt> <dd>

**Chaîne** contenant la lettre de lecteur suivie d’un signe deux-points («  : »).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **cdrom** .

## <a name="remarks"></a>Remarques

Les lettres de lecteur doivent être indiquées sous la forme *x*:, où *x* représente la lettre de lecteur.

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="examples"></a>Exemples

l’exemple de JScript suivant utilise *CdromCollection*. **getByDriveSpecifier** pour récupérer l’objet **cdrom** qui correspond à une lettre de lecteur fournie par l’utilisateur. Un élément de texte HTML a été créé, avec NAME = "MyText", pour l’entrée utilisateur. L’objet **Player** a été créé avec ID = "Player".


```JScript
// Store the drive letter provided by the user.
var DriveLetter = MyText.value;

// Append a colon to the drive letter to create a valid drive specifier.
DriveLetter += ":";

// Get the Cdrom object using the drive specifier.
var Drive = Player.cdRomCollection.getByDriveSpecifier(DriveLetter);

// Use the Cdrom object to open the drive door.
Drive.eject();
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet cdrom**](cdrom-object.md)
</dt> <dt>

[**Cdrom. éjecter**](cdrom-eject.md)
</dt> <dt>

[**Objet CdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





