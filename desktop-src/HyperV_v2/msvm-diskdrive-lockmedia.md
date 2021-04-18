---
description: Verrouille ou déverrouille le média.
ms.assetid: 805efb2d-71a7-4c74-821f-942644928ff9
title: Méthode LockMedia de la classe Msvm_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7ddc082ca6ceb7141eaa42bdfddf7a97897a9240
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522505"
---
# <a name="lockmedia-method-of-the-msvm_diskdrive-class"></a>Méthode LockMedia de la \_ classe DiskDrive MSVM

Verrouille ou déverrouille le média.

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

[**MSVM \_ DiskDrive**](msvm-diskdrive.md)
</dt> </dl>

 

 




