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
ms.openlocfilehash: 468bd6cdc8f3df7efba26997fd76b0724d3e4cc5da552275dad5201adc469f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906349"
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



 

## <a name="remarks"></a>Remarques

Cette méthode s’applique uniquement au volume du système d’exploitation, et uniquement si elle est effectivement suspendue à ce moment-là. Si le volume n’est pas suspendu ou n’est pas un volume du système d’exploitation, l' **erreur \_ non \_ prise en charge** est retournée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 Entreprise, Windows 8 Professionnel des \[ applications de bureau uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| En-tête<br/>                   | <dl> <dt>Activdbg. h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 




