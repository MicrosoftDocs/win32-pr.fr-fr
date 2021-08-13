---
title: Méthode IWMPSettings2 requestMediaAccessRights
description: La méthode requestMediaAccessRights demande un niveau d’accès spécifié à la bibliothèque. | Méthode IWMPSettings2 requestMediaAccessRights
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- Lecteur Windows Media de la méthode requestMediaAccessRights
- méthode requestMediaAccessRights Lecteur Windows Media, interface IWMPSettings2
- Lecteur Windows Media de l’interface IWMPSettings2, méthode requestMediaAccessRights
topic_type:
- apiref
api_name:
- IWMPSettings2.requestMediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aba44540717059945f273be23d2e3c63b3c10cfc6d21d35ee1c4756ea1503708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568486"
---
# <a name="iwmpsettings2requestmediaaccessrights-method"></a>IWMPSettings2 :: requestMediaAccessRights, méthode

La méthode **requestMediaAccessRights** demande un niveau d’accès spécifié à la bibliothèque.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Boolean requestMediaAccessRights(
  System.String bstrDesiredAccess
);
```


```VB

Public Function requestMediaAccessRights( _
  ByVal bstrDesiredAccess As System.String _
) As System.Boolean
Implements IWMPSettings2.requestMediaAccessRights
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrDesiredAccess* \[ dans\]
</dt> <dd>

**System. String** qui est l’une des valeurs suivantes.



| Valeur | Description                      |
|-------|----------------------------------|
| aucun  | Droits d’accès à l’élément actuel uniquement. |
| lire  | Droits d’accès en lecture uniquement.         |
| complet  | Droits d’accès en lecture/écriture.        |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. Boolean** qui indique si les droits d’accès demandés ont été accordés.

## <a name="remarks"></a>Remarques

Une page Web doit tout d’abord demander l’autorisation à l’utilisateur de lire des informations ou d’écrire des données dans la bibliothèque. L’appel de cette méthode invite l’utilisateur à utiliser une boîte de dialogue qui demande le niveau d’autorisation spécifié. Cela signifie que certaines méthodes, propriétés et événements seront inaccessibles à partir du code si les droits d’accès appropriés n’ont pas été accordés. Le niveau de droits d’accès actuel peut être récupéré à l’aide de **IWMPSettings2. mediaAccessRights**.

Les applications qui s’exécutent sur l’ordinateur de l’utilisateur ne sont pas tenues d’utiliser cette méthode.

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

[**IWMPSettings2. mediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





