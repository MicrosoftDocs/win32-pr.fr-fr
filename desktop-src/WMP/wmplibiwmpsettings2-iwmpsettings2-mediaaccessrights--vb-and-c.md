---
title: IWMPSettings2 propriété mediaAccessRights
description: La propriété mediaAccessRights obtient une valeur indiquant les autorisations actuellement accordées pour l’accès à la bibliothèque.
ms.assetid: c4289a2c-e343-405d-9bf5-0e97f6617916
keywords:
- Lecteur Windows Media de la propriété mediaAccessRights
- Lecteur Windows Media de la propriété mediaAccessRights, interface IWMPSettings2
- Lecteur Windows Media de l’interface IWMPSettings2, propriété mediaAccessRights
topic_type:
- apiref
api_name:
- IWMPSettings2.mediaAccessRights
- IWMPSettings2.get_mediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 797e45c62b505033afd2126f79d5830de5bc9847a4de36199a6c919a4978f112
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122489"
---
# <a name="iwmpsettings2mediaaccessrights-property"></a>IWMPSettings2 :: mediaAccessRights, propriété

La propriété **mediaAccessRights** obtient une valeur indiquant les autorisations actuellement accordées pour l’accès à la bibliothèque.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String mediaAccessRights {get;}
```


```VB

Public ReadOnly Property mediaAccessRights As System.String
```





## <a name="property-value"></a>Valeur de la propriété

**System. String** qui est l’une des valeurs suivantes.



| Valeur | Description                      |
|-------|----------------------------------|
| aucun  | Droits d’accès à l’élément actuel uniquement. |
| lire  | Droits d’accès en lecture uniquement.         |
| complet  | Droits d’accès en lecture/écriture.        |



 

## <a name="remarks"></a>Remarques

Une page Web doit tout d’abord demander l’autorisation à l’utilisateur de lire des informations ou d’écrire des données dans la bibliothèque. Cela signifie que certaines méthodes, propriétés et événements seront inaccessibles à partir du code si les droits d’accès appropriés n’ont pas été accordés. Pour obtenir les droits d’accès, l’application appelle **IWMPSettings2. obtenir \_ requestMediaAccessRights**, en passant un paramètre qui spécifie le niveau de droits d’accès souhaité.

Les applications qui s’exécutent sur l’ordinateur de l’utilisateur disposent toujours de droits d’accès complets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPSettings2 (VB et C#)**](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





