---
title: méthode Paramètres. requestMediaAccessRights
description: La méthode requestMediaAccessRights demande un niveau d’accès spécifié à la bibliothèque. | méthode Paramètres. requestMediaAccessRights
ms.assetid: 076b749b-9b25-483c-aa1f-60fc4367e4e0
keywords:
- Lecteur Windows Media de la méthode requestMediaAccessRights
- Lecteur Windows Media de la méthode requestMediaAccessRights, classe Paramètres
- Paramètres de la classe Lecteur Windows Media, méthode requestMediaAccessRights
topic_type:
- apiref
api_name:
- Settings.requestMediaAccessRights
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e157e7b4495c8d90964d62a9045eebb202126906f0022e97c4983220e47ac03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569310"
---
# <a name="settingsrequestmediaaccessrights-method"></a>méthode Paramètres. requestMediaAccessRights

La méthode **requestMediaAccessRights** demande un niveau d’accès spécifié à la bibliothèque.

## <a name="syntax"></a>Syntaxe


```JScript
bRetVal = Settings.requestMediaAccessRights(
  access
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*accès* \[ dans\]
</dt> <dd>

**Chaîne** spécifiant le niveau de droits d’accès souhaité. Contient l'une des valeurs suivantes :



| String | Description                      |
|--------|----------------------------------|
| aucun   | Droits d’accès à l’élément actuel uniquement. |
| lire   | Droits d’accès en lecture uniquement.         |
| complet   | Droits d’accès en lecture/écriture.        |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne une valeur **booléenne** indiquant si les droits d’accès demandés ont été accordés.

## <a name="remarks"></a>Notes

Une page Web doit tout d’abord demander l’autorisation à l’utilisateur de lire des informations ou d’écrire des données dans la bibliothèque. L’appel de cette méthode invite l’utilisateur à utiliser une boîte de dialogue qui demande le niveau d’autorisation spécifié. Cela signifie que certaines méthodes, propriétés et événements seront inaccessibles à partir du code si les droits d’accès appropriés n’ont pas été accordés. le niveau de droits d’accès actuel peut être récupéré à l’aide de *Paramètres*. **mediaAccessRights**.

**Lecteur Windows Media 10 Mobile**: cette méthode retourne toujours **true**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Paramètres Dessin**](settings-object.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> </dl>

 

 





