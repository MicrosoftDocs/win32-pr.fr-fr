---
description: Récupère le nombre de fois que BitLocker a été interrompu.
ms.assetid: B8C87352-62BA-4E5D-A273-CE74F3E1A7A8
title: Méthode GetSuspendCount de la classe Win32_EncryptableVolume (Activdbg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetSuspendCount
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eb28f019674f39946674399f8931fb63421ef982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545020"
---
# <a name="getsuspendcount-method-of-the-win32_encryptablevolume-class"></a>Méthode GetSuspendCount de la \_ classe Win32 EncryptableVolume

La méthode **GetSuspendCount** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) récupère le nombre de redémarrages avant que la protection ne soit reprise automatiquement.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetSuspendCount(
   uint32 SuspendCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SuspendCount* 
</dt> <dd>

Valeur entière comprise entre 0 et 15.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code de retour                                                                                          | Description                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                 | La méthode a réussi.<br/>                                      |
| <dl> <dt>**ERREUR \_ non \_ prise en charge**</dt> </dl> | Retourné si le volume n’est pas suspendu ou s’il ne s’agit pas d’un volume de système d’exploitation.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode s’applique uniquement au volume du système d’exploitation, et uniquement si elle est effectivement suspendue à ce moment-là. Si le volume n’est pas suspendu ou n’est pas un volume du système d’exploitation, l' **erreur \_ non \_ prise en charge** est retournée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 entreprise, applications de bureau Windows 8 professionnel \[ uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| En-tête<br/>                   | <dl> <dt>Activdbg. h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 




