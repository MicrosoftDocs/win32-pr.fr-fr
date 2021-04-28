---
description: 'Méthode LockMedia de la classe Msvm_DVDDrive : verrouille ou libère le média.'
ms.assetid: 924bc20a-901b-4618-be49-eaacf80c9465
title: Méthode LockMedia de la classe Msvm_DVDDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e00780fbeeeec60563b31008c8e5979a09f9d173
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119147"
---
# <a name="lockmedia-method-of-the-msvm_dvddrive-class"></a>Méthode LockMedia de la \_ classe DVDDrive MSVM

Verrouille ou libère le média.

## <a name="syntax"></a>Syntaxe


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Verrou* \[ dans\]
</dt> <dd>

**true** pour verrouiller le média ; **false** pour libérer le média.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

La méthode retourne l'une des valeurs suivantes :

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ DVDDrive**](msvm-dvddrive.md)
</dt> </dl>

 

 




