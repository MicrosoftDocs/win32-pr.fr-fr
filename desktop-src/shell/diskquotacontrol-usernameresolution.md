---
description: Définit ou obtient une valeur qui contrôle le mode de résolution de l’identificateur de sécurité (SID) de l’utilisateur en noms d’utilisateurs.
title: DiskQuotaControl. UserNameResolution, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.UserNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: dc936421-e66d-4762-912a-c586f9cdace4
ms.openlocfilehash: cfc86f7f7da03ea4ffb092d50b51ef0c69349935cdae40586e08ae50f6ea251b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224612"
---
# <a name="diskquotacontrolusernameresolution-property"></a>DiskQuotaControl. UserNameResolution, propriété

Définit ou obtient une valeur qui contrôle le mode de résolution de l’identificateur de sécurité (SID) de l’utilisateur en noms d’utilisateurs.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a>Valeur de la propriété

Cette propriété peut être définie sur l’une des valeurs suivantes.



| Type de résolution | Valeur | Description                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| dqResolveNone   | 0     | Ne résolvez pas les informations de nom d’utilisateur.                                                                                                                    |
| dqResolveSync   | 1     | Veuillez patienter pendant la résolution des informations de nom.                                                                                                                   |
| dqResolveAsync  | 2     | N’attendez pas la résolution des informations de nom. L’événement [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) se déclenche lorsque le nom est résolu. |



 

## <a name="remarks"></a>Remarques

Cette propriété affecte l’énumération des objets [**DIDiskQuotaUser**](didiskquotauser-object.md) , ainsi que les méthodes [**adduser**](diskquotacontrol-adduser.md) et [**FindUser**](diskquotacontrol-finduser.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




