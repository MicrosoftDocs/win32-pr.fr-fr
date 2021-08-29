---
description: 'Méthode LockMedia de la classe Msvm_DisketteDrive : verrouille ou libère le média.'
ms.assetid: 90f7e06c-92d0-4742-a74d-68ae6bfc00bf
title: Méthode LockMedia de la classe Msvm_DisketteDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31cdddccf5a62c5f26f83351977090fa5c5a33e24476a3de4e88ee5e40938f8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119431029"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a>Méthode LockMedia de la \_ classe DisketteDrive MSVM

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

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite ; Sinon, retourne l’une des valeurs suivantes :

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

[**MSVM \_ DisketteDrive**](msvm-diskettedrive.md)
</dt> </dl>

 

 




