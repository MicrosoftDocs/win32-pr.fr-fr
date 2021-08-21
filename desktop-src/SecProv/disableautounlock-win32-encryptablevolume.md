---
description: Supprime la clé externe enregistrée sur le volume du système d’exploitation en cours d’exécution.
ms.assetid: a8c4bb3b-6566-4173-b550-e89740f1cba6
title: Méthode DisableAutoUnlock de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: ce3a6bbb396136b128e084da0e64a79ad2f403217d8ac51dcf67b57941cc4a4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004557"
---
# <a name="disableautounlock-method-of-the-win32_encryptablevolume-class"></a>Méthode DisableAutoUnlock de la \_ classe Win32 EncryptableVolume

La méthode **DisableAutoUnlock** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) supprime la clé externe enregistrée sur le volume du système d’exploitation en cours d’exécution afin qu’un volume de données ne soit pas automatiquement déverrouillé lorsqu’il est monté, par exemple lorsque des périphériques mémoire amovibles sont connectés à l’ordinateur.

Si le déverrouillage automatique est désactivé ou suspendu, les méthodes [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) ou [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) doivent être utilisées pour déverrouiller le volume.

## <a name="syntax"></a>Syntaxe


```mof
uint32 DisableAutoUnlock();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.



| Code/valeur de retour                                                                                                                                                                       | Description                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | La méthode a réussi.<br/>                                                       |
| <dl> <dt> **\_ Volume FVE \_ E \_ non \_ lié**</dt> <dt>2150694935 (0x80310017)</dt> </dl> | Le déverrouillage automatique sur le volume est désactivé.<br/>                                   |
| <dl> <dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt> </dl>      | BitLocker n’est pas activé sur le volume. Ajoutez un protecteur de clé pour activer BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ non \_ \_ VOLUME de données**</dt> <dt>2150694937 (0x80310019)</dt> </dl>   | La méthode ne peut pas être exécutée pour le volume du système d’exploitation en cours d’exécution.<br/>      |



 

## <a name="remarks"></a>Remarques

Si aucune erreur n’est retournée, cette méthode supprime du Registre tous les ID de protecteur de volume et les clés externes utilisés pour déverrouiller automatiquement le volume.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista Enterprise, Windows les applications de bureau vista Ultimate \[ uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
